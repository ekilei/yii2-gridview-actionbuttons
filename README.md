# yii2-gridview-actionbuttons
Widget for Yii2 GridView Action Column, for adaptive versions, it is convenient to use on desktop and smartphone

Виждет для Yii2 GridView ActionColumn, для адаптивных версий, удобно в использовании на десктопе и смартфоне

### Замена обычных кнопок на выпадающее меню производится сравнительно легко 

Replacement of conventional buttons on the drop-down menu will be relatively easy
```$xslt
<?= GridView::widget([
    'dataProvider' => $dataProvider,
    'columns' => [
        //['class' => 'yii\grid\ActionColumn',],
        ['class' => 'common\widgets\ActionButtons'],
        'name',
    ],
]); ?>
```

### По умолчанию набор кнопок стандратный, однако их можно изменять, тут есть отличие от стандартного ActionColumn

By default, the set of buttons is standard, but you can to change, here there is a difference from standard ActionColumn

![ScreenShot](https://raw.github.com/ekilei/yii2-viewgrid-actionbuttons/master/docfiles/1.png)

![ScreenShot](https://raw.github.com/ekilei/yii2-viewgrid-actionbuttons/master/docfiles/2.png)


### Вариант, когда какая-то кнопка не нужна.

Option, when a button is not needed.

![ScreenShot](https://raw.github.com/ekilei/yii2-viewgrid-actionbuttons/master/docfiles/3.png)
```$xslt
['class' => '\common\widgets\ActionButtons','exclude' => ['view']],
```


### Вариант, когда кнопку по умолчанию надо переставить на другую.

Option, when the default button should be rearranged to another.

![ScreenShot](https://raw.github.com/ekilei/yii2-viewgrid-actionbuttons/master/docfiles/4.png)
```$xslt
['class' => '\common\widgets\ActionButtons','default' => 'update'],
```


### Вариант, когда надо переписать блок кнопок своими. При использовании своих кнопок, кнопки по умолчанию игнорируются.

Option, when you need to rewrite the button block with your own. When using their buttons, the buttons are ignored by default.

![ScreenShot](https://raw.github.com/ekilei/yii2-viewgrid-actionbuttons/master/docfiles/5.png)
```$xslt
['class' => 'common\widgets\ActionButtons','buttons' => [
    'list' => 'th-list',
    'shutdown' => [
        'icon' => 'off',
        'method' => 'post',
        'confirm' => Yii::t('yii', 'Are you sure you want to disable this item?'),
    ]
]],
```
> **Note:** В данном случае ключ массива служит командой действия.
Значение имеет два состояния: если строка, то это иконка по стандарту Glyphicons,
если массив, то параметры.

> **Note:** In this case, the array key serves as an action command.
The value has two states: if the string, then this is the icon for the standard Glyphicons,
If the array, then the parameters.


### Кнопки можно стилизовать. Отдельно кнопку по умолчанию и отдельно кнопку выпадения меню.

Buttons can be stylized. Separately, the default button and a separate drop-down menu button. 

![ScreenShot](https://raw.github.com/ekilei/yii2-viewgrid-actionbuttons/master/docfiles/6.png)
```$xslt
['class' => '\common\widgets\ActionButtons',
    'style_drop' => '',
    'style_def' => 'border-radius:0;'
],
```
 