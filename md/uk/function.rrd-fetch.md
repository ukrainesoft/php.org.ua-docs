---
navigation:
  - function.rrd-error.md: « rrderror
  - function.rrd-first.md: rrdfirst »
  - index.md: PHP Manual
  - ref.rrd.md: Функції RRD
title: rrdfetch
---
# rrdfetch

(PECL rrd >= 0.9.0)

rrdfetch — Витягти дані для графіка у вигляді масиву

### Опис

```methodsynopsis
rrd_fetch(string $filename, array $options): array
```

Витягує дані для графіка як масиву з файлу RRD. Функція працює так само як і [rrdgraph()](function.rrd-graph.md), але дані повертаються як масиву, а зображення не створюється.

### Список параметрів

`filename`

Назва файлу RRD.

`options`

Масив опцій для специфікації дозволу.

### Значення, що повертаються

Вилучений масив даних.
