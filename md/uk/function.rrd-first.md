---
navigation:
  - function.rrd-fetch.md: « rrd\_fetch
  - function.rrd-graph.md: rrd\_graph »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_first
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_first

(PECL rrd >= 0.9.0)

rrd\_first — Повертає позначку першого зразка з файлу rrd

### Опис

```methodsynopsis
rrd_first(string $file, int $raaindex = 0): int
```

Повертає перший зразок даних із вказаного RRA файлу RRD.

### Список параметрів

`file`

Назва файлу бази даних RRD.

`raaindex`

Номер індексу RRA, який має бути розглянутий. Значення за промовчанням - 0.

### Значення, що повертаються

Номер позначки часу unix у вигляді цілого чи числа \*\*`false`\*\*в случае возникновения ошибки.
