# yii2-viewgrid-actionbuttons
Widget for Yii2 ViewGrid ActionColumn

Replacement of conventional buttons on the drop-down menu will be relatively easy

Замена обычных кнопок на выпадабщее меню произвится сравнительно легко 
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

