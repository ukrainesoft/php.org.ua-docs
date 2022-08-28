Процедурний приклад PECL/rrd

-   [« Примеры](rrd.examples.html)
    
-   [Объектно-ориентированный пример PECL/rrd »](rrd.examples-oop.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](rrd.examples.html)
    
-   Процедурний приклад PECL/rrd
    

## Процедурний приклад PECL/rrd

**Приклад #1 Використання rrd у процедурному стилі**

```php
<?php
$rrdFile = dirname(__FILE__) . "/speed.rrd";

//создание файла rrd
rrd_create($rrdFile,
 array(
  "--start",920804400,
  "DS:speed:COUNTER:600:U:U",
  "RRA:AVERAGE:0.5:1:24",
  "RRA:AVERAGE:0.5:6:10"
  )
);

//обновление файла rrd
rrd_update($rrdFile,
 array(
  "920804700:12345",
  "920805000:12357"
  )
);

//вывод графика
rrd_graph(dirname(__FILE__) . "/speed.png",
 array(
  "--start", "920804400",
  "--end", "920808000",
  "--vertical-label", "m/s",
  "DEF:myspeed=$rrdFile:speed:AVERAGE",
  "CDEF:realspeed=myspeed,1000,*",
  "LINE2:realspeed#FF0000"
 )
);
?>
```