DetailView4cols Extension for Yii2
==================================
This extension is a variation of the DetailView widget of Yii2. It has simply the same code with a few modification to it.
Thanks to "Yii 1.1: detailview4col (Developed by: [c@cba](http://www.yiiframework.com/user/54420/)) extension".
Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist gamitg/yii2-detailview4cols "*"
```

or add

```
"gamitg/yii2-detailview4cols": "*"
```

to the require section of your `composer.json` file.

Note
----
If you getting while installing this extension, so just add following line in your `composer.json` file.

```
"minimum-stability": "dev",
"prefer-stable": true,
```

Because of this extension currently available only in `dev-master`. So, i appreciate your suggestion and also issue fixing related to this extension.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
<?= \gamitg\detailview4cols\DetailView4Col::widget(); ?>
```

Example
-------

```php
	<?= \gamitg\detailview4cols\DetailView4Col::widget([
		        'model' => $model,
		        'options'=>['class'=>'table table-striped table-bordered detail-view'],
		        'attributes' => [
					'id',
					[
		        		'attribute' => 'user_id',
		        		'value' => $model->user->user_name,
		        		'oneRow' =>true
					],
			        'page_id',
			        'comment:ntext',
			        'time:datetime',
			        [
					   	'attribute'=>'created_by',
						'value'=>(!empty($model->user_id) ? $model->user_id : "Not Set")
				    ],
		        ],
    	]) ?>
```
