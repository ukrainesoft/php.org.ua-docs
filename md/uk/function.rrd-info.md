---
navigation:
  - function.rrd-graph.md: « rrdgraph
  - function.rrd-last.md: rrdlast »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrdinfo
---
# rrdinfo

(PECL rrd >= 0.9.0)

rrdinfo — Отримує інформацію про файл rrd

### Опис

```methodsynopsis
rrd_info(string $filename): array
```

Повертає інформацію про вказаний файл бази даних RRD.

### Список параметрів

`file`

Назва файлу бази даних RRD.

### Значення, що повертаються

Масив, що містить інформацію про вказаний файл RRD або **`false`** у разі виникнення помилки.
