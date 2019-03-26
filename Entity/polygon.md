polygon : PolygonGraphics
```
var bluePolygon = viewer.entities.add({
    name : 'Blue polygon with holes',
    polygon : {
        hierarchy : {
            positions : Cesium.Cartesian3.fromDegreesArray([-99.0, 30.0,
                                                            -85.0, 30.0,
                                                            -85.0, 40.0,
                                                            -99.0, 40.0]),
            holes : [{
                positions : Cesium.Cartesian3.fromDegreesArray([
                    -97.0, 31.0,
                    -97.0, 39.0,
                    -87.0, 39.0,
                    -87.0, 31.0
                ]),
                holes : [{
                    positions : Cesium.Cartesian3.fromDegreesArray([
                        -95.0, 33.0,
                        -89.0, 33.0,
                        -89.0, 37.0,
                        -95.0, 37.0
                    ]),
                    holes : [{
                        positions : Cesium.Cartesian3.fromDegreesArray([
                            -93.0, 34.0,
                            -91.0, 34.0,
                            -91.0, 36.0,
                            -93.0, 36.0
                        ])
                    }]
                }]
            }]
        },
        material : Cesium.Color.BLUE.withAlpha(0.5),
        height : 0,
        outline : true // height is required for outline to display
    }
});
```
