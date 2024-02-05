---
navigation:
  - function.rrd-graph.md: « rrd\_graph
  - function.rrd-last.md: rrd\_last »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_info

(PECL rrd >= 0.9.0)

rrd\_info — Отримує інформацію про файл rrd

### Опис

```methodsynopsis
rrd_info(string $filename): array
```

Повертає інформацію про вказаний файл бази даних RRD.

### Список параметрів

`file`

Назва файлу бази даних RRD.

### Значення, що повертаються

Масив, що містить інформацію про вказаний файл RRD або \*\*`false`\*\*в случае возникновения ошибки.
