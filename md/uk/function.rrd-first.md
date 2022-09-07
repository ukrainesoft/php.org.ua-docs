---
navigation:
  - function.rrd-fetch.md: « rrdfetch
  - function.rrd-graph.md: rrdgraph »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrdfirst
---
# rrdfirst

(PECL rrd >= 0.9.0)

rrdfirst — Повертає позначку першого зразка з файлу rrd

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

Номер позначки часу unix у вигляді цілого чи числа **`false`** у разі виникнення помилки.
