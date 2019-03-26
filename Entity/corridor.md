corridor : CorridorGraphics
```
var blueCorridor = viewer.entities.add({
    name : 'Blue extruded corridor with beveled corners and outline',
    corridor : {
        positions : Cesium.Cartesian3.fromDegreesArray([
                                                        -80.0, 40.0,
                                                        -85.0, 40.0,
                                                        -85.0, 35.0
                                                    ]),//[longitude, latitude, longitude, latitude...]
        height : 200000.0,
        extrudedHeight : 100000.0,
        width : 200000.0,
        cornerType: Cesium.CornerType.BEVELED,//转角类型：BEVELED/MITERED/ROUNDED(default)
        material : Cesium.Color.BLUE.withAlpha(0.5),
        outline : true, // height or extrudedHeight must be set for outlines to display
        outlineColor : Cesium.Color.WHITE
    }
});
```
