### 一.时间转换时间戳
```sh
           function transdate(endTime){
                        var date=new Date();
                        date.setFullYear(endTime.substring(0,4));
                        date.setMonth(endTime.substring(5,7)-1);
                        date.setDate(endTime.substring(8,10));
                        date.setHours(endTime.substring(11,13));
                        date.setMinutes(endTime.substring(14,16));
                        date.setSeconds(endTime.substring(17,19));
                        return Date.parse(date)/1000;
            }
```


### 二.时间戳转换时间

>1 转换成 2011-3-16 16:50:43 格式

```sh
     function getDate(tm){
            var tt=new Date(parseInt(tm) * 1000).toLocaleString().replace(/年|月/g, "-").replace(/日/g, " ")
            return tt;
      }
```

>2 转换成 2011年3月16日 16:50:43 格式

```sh
function getDate(tm){
            var tt=new Date(parseInt(tm) * 1000).toLocaleString()
            return tt;
}
```

>3 转换成 2011年3月16日 16:50

```sh
function getDate(tm){
            var tt=new Date(parseInt(tm) * 1000).toLocaleString().substr(0,16);
            return tt;
}
```
