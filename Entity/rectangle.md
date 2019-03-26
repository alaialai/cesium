rectangle : RectangleGraphics
```
var greenRectangle = viewer.entities.add({
    name : 'Green translucent, rotated, and extruded rectangle at height with outline',
    rectangle : {
        coordinates : Cesium.Rectangle.fromDegrees(-110.0, 30.0, -100.0, 40.0),//Cesium.Rectangle.fromDegrees(west, south, east, north, result) → Rectangle
        material : Cesium.Color.GREEN.withAlpha(0.5),
        rotation : Cesium.Math.toRadians(45),
        extrudedHeight : 300000.0,
        height : 100000.0,
        outline : true, // height must be set for outline to display
        outlineColor : Cesium.Color.BLACK
    }
});

var rotation = Cesium.Math.toRadians(30);

function getRotationValue() {
    rotation += 0.005;
    return rotation;
}
viewer.entities.add({
    name: 'Rotating rectangle with rotating texture coordinate',
    rectangle: {
        coordinates: Cesium.Rectangle.fromDegrees(-92.0, 30.0, -76.0, 40.0),
        material: '../images/Cesium_Logo_Color.jpg',
        rotation: new Cesium.CallbackProperty(getRotationValue, false),//new Cesium.CallbackProperty(callback, isConstant) 矩形旋转
        stRotation: new Cesium.CallbackProperty(getRotationValue, false),//矩形纹理旋转
        classificationType : Cesium.ClassificationType.TERRAIN
    }
});
```
