---
navigation:
  - rrdgraph.saveverbose.md: '« RRDGraph::saveVerbose'
  - class.rrdupdater.md: RRDUpdater »
  - index.md: PHP Manual
  - class.rrdgraph.md: RRDGraph
title: 'RRDGraph::setOptions'
---
# RRDGraph::setOptions

(PECL rrd >= 0.9.0)

RRDGraph::setOptions — Встановлює параметри для експорту графіка rrd

### Опис

```methodsynopsis
public RRDGraph::setOptions(array $options): void
```

### Список параметрів

`options`

Список параметрів для створення зображення з файлу бази даних RRD. Це може бути список рядків або список рядків з ключами для кращого читання. Прочитайте довідкові сторінки rrd graph, щоб отримати список доступних параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **RRDGraph::setOptions()****

```php
<?php
$graphObj->setOptions(array(
    "--start" => "920804400",
    "--end" => 920808000,
    "--vertical-label" => "m/s",
    "DEF:myspeed=$rrdFile:speed:AVERAGE",
    "CDEF:realspeed=myspeed,1000,*",
    "LINE2:realspeed#FF0000"
));
?>
```

**Приклад #2 Встановлення кількох варіантів кольорів**

```php
<?php
$graphObj->setOptions(array(
    "--start" => "920804400",
    "--end" => 920808000,
    "--vertical-label" => "m/s",
    "--color=BACK#00000000",
    "--color=GRID#00000000",
    "--color=MGRID#00000000",
    "DEF:myspeed=$rrdFile:speed:AVERAGE",
    "CDEF:realspeed=myspeed,1000,*",
    "LINE2:realspeed#FF0000"
));
?>
```

Не використовуйте синтаксис ключ-значення для однакових опцій rrd. Виглядає більш читабельно, але не працює.

```php
<?php
$graphObj->setOptions(array(
    "--color" => "BACK#00000000",
    "--color" => "GRID#00000000",
    "--color" => "MGRID#00000000"
));
?>
```

Приклад вище означає те саме.

```php
<?php
$graphObj->setOptions(array(
    "--color" => "MGRID#00000000"
));
?>
```
