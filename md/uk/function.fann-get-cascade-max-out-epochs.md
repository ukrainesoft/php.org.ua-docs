---
navigation:
  - function.fann-get-cascade-max-cand-epochs.md: « fann\_get\_cascade\_max\_cand\_epochs
  - function.fann-get-cascade-min-cand-epochs.md: fann\_get\_cascade\_min\_cand\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_max\_out\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_max\_out\_epochs

(PECL fann >= 1.0.0)

fann\_get\_cascade\_max\_out\_epochs — Повертає максимальну кількість періодів

### Опис

```methodsynopsis
fann_get_cascade_max_out_epochs(resource $ann): int
```

Максимальна кількість періодів визначає кількість періодів, у яких вихідні з'єднання можуть бути навчені після додавання нового нейрона-кандидата.

Максимальна кількість періодів дорівнює 150.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Максимальна кількість періодів або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_max\_out\_epochs()](function.fann-set-cascade-max-out-epochs.md) \- Встановлює максимальну кількість епох
