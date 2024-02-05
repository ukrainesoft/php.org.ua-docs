---
navigation:
  - function.fann-get-cascade-output-stagnation-epochs.md: « fann\_get\_cascade\_output\_stagnation\_epochs
  - function.fann-get-connection-array.md: fann\_get\_connection\_array »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_weight\_multiplier
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_weight\_multiplier

(PECL fann >= 1.0.0)

fann\_get\_cascade\_weight\_multiplier — Повертає множник ваги

### Опис

```methodsynopsis
fann_get_cascade_weight_multiplier(resource $ann): float
```

Множник ваги - це параметр, який використовується для множення ваги нейрона-кандидата перед додаванням нейрона до нейронної мережі. Цей параметр зазвичай знаходиться в діапазоні від 0 до 1 і використовується, щоб зробити тренування менш агресивним.

Множник ваги за промовчанням дорівнює 0.4.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Множитель веса или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_weight\_multiplier()](function.fann-set-cascade-weight-multiplier.md) \- Встановлює множник ваги
