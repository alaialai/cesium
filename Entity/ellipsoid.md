ellipsoid : EllipsoidGraphics
```
var outlineOnly = viewer.entities.add({
    name : 'Yellow ellipsoid outline',
    position: Cesium.Cartesian3.fromDegrees(-100.0, 40.0, 300000.0),
    ellipsoid : {
        radii : new Cesium.Cartesian3(200000.0, 200000.0, 300000.0),
        fill : false,
        outline : true,
        outlineColor : Cesium.Color.YELLOW,
        slicePartitions : 24,//竖着切割成24块
        stackPartitions : 36//横着切割成36块
    }
});
```
