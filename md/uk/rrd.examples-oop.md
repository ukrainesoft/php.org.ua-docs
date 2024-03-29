---
navigation:
  - rrd.examples-procedural.md: « Процедурний приклад PECL/rrd
  - ref.rrd.md: Функції RRD »
  - index.md: PHP Manual
  - rrd.examples.md: Приклади
title: Об'єктно-орієнтований приклад PECL/rrd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Об'єктно-орієнтований приклад PECL/rrd

**Приклад #1 Використання rrd в об'єктно-орієнтованому стилі**

```php
<?php
$rrdFile = dirname(__FILE__) . "/speed.rrd";
$outputPngFile = dirname(__FILE__) . "/speed.png";

$creator = new RRDCreator($rrdFile, "now -10d", 500);
$creator->addDataSource("speed:COUNTER:600:U:U");
$creator->addArchive("AVERAGE:0.5:1:24");
$creator->addArchive("AVERAGE:0.5:6:10");
$creator->save();

$updater = new RRDUpdater($rrdFile);
$updater->update(array("speed" => "12345"), "920804700");
$updater->update(array("speed" => "12357"), "920805000");

$graphObj = new RRDGraph($outputPngFile);
$graphObj->setOptions(
    array(
        "--start" => "920804400",
        "--end" => 920808000,
        "--vertical-label" => "m/s",
        "DEF:myspeed=$rrdFile:speed:AVERAGE",
        "CDEF:realspeed=myspeed,1000,*",
        "LINE2:realspeed#FF0000"
    )
);
$graphObj->save();
?>
```
