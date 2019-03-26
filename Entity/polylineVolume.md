polylineVolume : PolylineVolumeGraphics
```
function computeStar(arms, rOuter, rInner) {
    var angle = Math.PI / arms;
    var length = 2 * arms;
    var positions = new Array(length);
    for (var i = 0; i < length; i++) {
        var r = (i % 2) === 0 ? rOuter : rInner;
        positions[i] = new Cesium.Cartesian2(Math.cos(i * angle) * r, Math.sin(i * angle) * r);
    }
    return positions;
}

var blueStar = viewer.entities.add({
    name : 'Blue star with mitered corners and outline',
    polylineVolume : {
        positions : Cesium.Cartesian3.fromDegreesArrayHeights([-95.0, 32.0, 0.0,
                                                               -95.0, 36.0, 100000.0,
                                                               -99.0, 36.0, 200000.0]),
        shape : computeStar(7, 70000, 50000),
        cornerType : Cesium.CornerType.MITERED,
        material : Cesium.Color.BLUE
    }
});
```
