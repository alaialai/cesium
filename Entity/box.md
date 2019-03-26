box : BoxGraphics
```
var viewer = new Cesium.Viewer('cesiumContainer');

var redBox = viewer.entities.add({
    name : 'Red box with black outline',
    position: Cesium.Cartesian3.fromDegrees(-107.0, 40.0, 300000.0),//规格
    box : {
        dimensions : new Cesium.Cartesian3(400000.0, 300000.0, 500000.0),//长，宽，高
        material : Cesium.Color.RED.withAlpha(0.5),
        outline : true,
        outlineColor : Cesium.Color.BLACK
    }
});//添加实体对象（红色填充）

var outlineOnly = viewer.entities.add({
    name : 'Yellow box outline',
    position: Cesium.Cartesian3.fromDegrees(-100.0, 40.0, 300000.0),
    box : {
        dimensions : new Cesium.Cartesian3(400000.0, 300000.0, 500000.0),
        fill : false,
        outline : true,
        outlineColor : Cesium.Color.YELLOW
    }
});//添加实体对象（无填充）

viewer.zoomTo(viewer.entities);//显示实体
```
