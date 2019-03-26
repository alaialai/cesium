cylinder : CylinderGraphics
```
var redCone = viewer.entities.add({
    name : 'Red cone',
    position: Cesium.Cartesian3.fromDegrees(-105.0, 40.0, 200000.0),
    cylinder : {
        length : 800000.0,//高度
        topRadius : 0.0,
        bottomRadius : 200000.0,
        material : Cesium.Color.RED
    }
});
```
