- [« RRDGraph::saveVerbose](rrdgraph.saveverbose.md)
- [RRDUpdater »](class.rrdupdater.md)

- [PHP Manual](index.md)
- [RRDGraph](class.rrdgraph.md)
- Встановлює параметри експорту графіка rrd

# RRDGraph::setOptions

(PECL rrd \>= 0.9.0)

RRDGraph::setOptions — Встановлює параметри експорту графіка rrd

### Опис

public **RRDGraph::setOptions**(array `$options`): void

### Список параметрів

`options`
Список параметрів для створення зображення з файлу бази даних RRD.
Це може бути список рядків або список рядків із ключами для кращої
читання. Прочитайте довідкові сторінки rrd graph для отримання списку
параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **RRDGraph::setOptions()****

` <?php$graphObj->setOptions(array(    "--start" => "920804400",    "--end" => 920808000,    "--vertical-label myspeed=$rrdFile:speed:AVERAGE",    "CDEF:realspeed=myspeed,1000,*",   "LINE2:realspeed#FF0000"));?> `

**Приклад #2 Встановлення кількох варіантів кольорів**

` <?php$graphObj->setOptions(array(   "--start" => "920804400",    "--end" => 920808000,    "--vertical-label| " color=BACK#00000000",   "--color=GRID#00000000",   "--color=MGRID#00000000",    "DEF:myspeed=$rrdFile:speed:AVERAGE" ",    "LINE2:realspeed#FF0000"));?> `

Не використовуйте синтаксис ключ-значення для однакових опцій rrd.
Виглядає більш читально, але не працює.

` <?php$graphObj->setOptions(array(    "--color" => "BACK#00000000",     ---color" =>"GRID#00000000",  00"0 0" ));?> `

Приклад вище означає те саме.

` <?php$graphObj->setOptions(array(    "--color" => "MGRID#00000000"));?> `
