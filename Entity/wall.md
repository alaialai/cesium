wall : WallGraphics
```
var blueWall = viewer.entities.add({
    name : 'Blue wall with sawtooth heights and outline',
    wall : {
        positions : Cesium.Cartesian3.fromDegreesArray([-115.0, 50.0,
                                                        -112.5, 50.0,
                                                        -110.0, 50.0,
                                                        -107.5, 50.0,
                                                        -105.0, 50.0,
                                                        -102.5, 50.0,
                                                        -100.0, 50.0,
                                                        -97.5, 50.0,
                                                        -95.0, 50.0,
                                                        -92.5, 50.0,
                                                        -90.0, 50.0]),
        maximumHeights : [100000, 200000, 100000, 200000, 100000, 200000, 100000, 200000, 100000, 200000, 100000],
        minimumHeights : [0, 100000,  0, 100000, 0, 100000, 0, 100000, 0, 100000, 0],
        material : Cesium.Color.BLUE.withAlpha(0.5),
        outline : true,
        outlineColor : Cesium.Color.BLACK
    }
});
```