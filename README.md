# time-sec
时分秒与秒之间的转换

1. 秒 转为 时分秒（00:00:00）

    ```
    var sec_to_time = function(s) {
        var t;
        if(s > -1){
            var hour = Math.floor(s/3600);
            var min = Math.floor(s/60) % 60;
            var sec = s % 60;
            if(hour < 10) {
                t = '0'+ hour + ":";
            } else {
                t = hour + ":";
            }

            if(min < 10){t += "0";}
            t += min + ":";
            if(sec < 10){t += "0";}
            t += sec;
        }
        return t;
    }
    ```



2. 时分秒（00:00:00） 转为 秒

    ```
    var time_to_sec = function (time) {
        var s = '';

        var hour = time.split(':')[0];
        var min = time.split(':')[1];
        var sec = time.split(':')[2];

        s = Number(hour*3600) + Number(min*60) + Number(sec);

        return s;
    };
    ```
