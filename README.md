yii2-treeimage
==============
view tree with image and dependecies with tree-manager

Example
------------
![example](https://raw.githubusercontent.com/soul714/yii2-treeimage/master/example/Screenshot%20from%202016-03-22%2018%3A37%3A05.png)


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist soul714/yii2-treeimage "dev-master"
```

or add

```
"soul714/yii2-treeimage": "dev-master"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
<?= \soul714\treeimage\TreeImage::widget(
    'query' => Tree::find()->addOrderBy('root, lft'), 
); ?>```