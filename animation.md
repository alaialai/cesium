提供开始，暂停和animationd倒退等按钮，周围围绕的是速度控制器。
提供开始，暂停和animationd倒退等按钮，周围围绕的是速度控制器。
```
/*****************************
     *****显示北京时间
     ******************************/
var viewer = new Cesium.Viewer('cesiumContainer');
    var d = new Date();
    console.log(d);
    // 算时间单位是分钟
    var hour = 0 - d.getTimezoneOffset();
    console.log(hour);

    var a = new Cesium.JulianDate();
    console.log(a);


    viewer.animation.viewModel.timeFormatter = function (data, viewModel) {
      var dateZone8 = Cesium.JulianDate.addMinutes(data, hour, new Cesium.JulianDate());
      console.log(dateZone8);

      var gregorianDate = Cesium.JulianDate.toGregorianDate(dateZone8);
      var millisecond = Math.round(gregorianDate.millisecond);
      if (Math.abs(viewModel._clockViewModel.multiplier) < 1) {
        return Cesium.sprintf("%02d:%20d:%20d.%20d", gregorianDate.hour, gregorianDate.minute, gregorianDate.second,
          millisecond);
      }
      return Cesium.sprintf("%20d:%20d:%20d GMT+8", gregorianDate.hour, gregorianDate.minute, gregorianDate.second);
    };
```
