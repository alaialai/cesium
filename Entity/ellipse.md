ellipse : EllipseGraphics
```
var blueEllipse = viewer.entities.add({
    position: Cesium.Cartesian3.fromDegrees(-95.0, 40.0, 100000.0),
    name : 'Blue translucent, rotated, and extruded ellipse with outline',
    ellipse : {
        semiMinorAxis : 150000.0,
        semiMajorAxis : 300000.0,
        extrudedHeight : 200000.0,//形成椭圆体
				height: 100000.0,//离地面高度
        rotation : Cesium.Math.toRadians(45),
        material : Cesium.Color.BLUE.withAlpha(0.5),
        outline : true
    }
});
```
