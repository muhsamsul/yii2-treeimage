yii2-treeimage
==============
View tree with organizational chart. Dependencies with kartik tree manager

View example
------------
![example](https://raw.githubusercontent.com/muhsamsul/yii2-treeimage/master/example/Screenshot%20from%202016-03-22%2018%3A37%3A05.png)


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist muhsamsul/yii2-treeimage "dev-master"
```

or add

```
"muhsamsul/yii2-treeimage": "dev-master"
```

to the require section of your `composer.json` file.

Migration database or import tbl_tree.sql
-----
yii migrate/up --migrationPath=@vendor/muhsamsul/yii2-treeimage/migrations

or import sql file on directory = vendor/muhsamsul/yii2-treeimage/db/tbl_tree.sql

generete model with Table Prefix

How to create new and update data
-----
usage kartik tree-manager
[yii2-tree-manager](https://github.com/kartik-v/yii2-tree-manager)

Usage
-----

Once the extension is installed, simply use it in your code by  :

in your view file:
```php
use app\models\Tree;
use muhsamsul\treeimage\TreeImage;

<?= TreeImage::widget(
    'query' 	=> Tree::find()->addOrderBy('root, lft'), 
    'root'  	=> 'Parent',								//default parent
    'icon' 		=> 'user', 									//default user
    'iconRoot' 	=> 'tree-conifer', 							//default tree-conifer
); ?>