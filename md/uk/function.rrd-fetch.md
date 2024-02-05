---
navigation:
  - function.rrd-error.md: « rrd\_error
  - function.rrd-first.md: rrd\_first »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrd\_fetch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rrd\_fetch

(PECL rrd >= 0.9.0)

rrd\_fetch — Витягти дані для графіка у вигляді масиву

### Опис

```methodsynopsis
rrd_fetch(string $filename, array $options): array
```

Витягує дані для графіка як масиву з файлу RRD. Функція працює так само як і [rrd\_graph()](function.rrd-graph.md), але дані повертаються як масиву, а зображення не створюється.

### Список параметрів

`filename`

Ім'я файлу RRD.

`options`

Масив опцій для специфікації дозволу.

### Значення, що повертаються

Вилучений масив даних.
