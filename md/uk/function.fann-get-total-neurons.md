---
navigation:
  - function.fann-get-total-connections.md: « fann\_get\_total\_connections
  - function.fann-get-train-error-function.md: fann\_get\_train\_error\_function »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_total\_neurons
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_total\_neurons

(PECL fann >= 1.0.0)

fann\_get\_total\_neurons — Отримує загальну кількість нейронів у всій мережі

### Опис

```methodsynopsis
fann_get_total_neurons(resource $ann): int
```

Отримує загальну кількість нейронів у всій мережі. Число також включає нейрони усунення, тому мережа 2-4-2 має 2+4+2 +2 (зміщення) = 10 нейронів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Загальна кількість нейронів у всій мережі або \*\*`false`\*\*в случае возникновения ошибки.
