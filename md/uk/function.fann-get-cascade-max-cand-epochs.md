---
navigation:
  - function.fann-get-cascade-candidate-stagnation-epochs.md: « fann\_get\_cascade\_candidate\_stagnation\_epochs
  - function.fann-get-cascade-max-out-epochs.md: fann\_get\_cascade\_max\_out\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_max\_cand\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_max\_cand\_epochs

(PECL fann >= 1.0.0)

fann\_get\_cascade\_max\_cand\_epochs - Отримує найбільший період кандидата

### Опис

```methodsynopsis
fann_get_cascade_max_cand_epochs(resource $ann): int
```

Максимальний період кандидата визначає максимальну кількість періодів, у яких вхідні з'єднання з кандидатами можуть бути навчені перед додаванням нового нейрона-кандидата.

Максимальний період кандидата за умовчанням – 150.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Максимальний період кандидата чи \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_max\_cand\_epochs()](function.fann-set-cascade-max-cand-epochs.md) \- встановлює найбільший період кандидата
