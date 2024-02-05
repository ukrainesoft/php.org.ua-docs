---
navigation:
  - function.fann-get-cascade-candidate-change-fraction.md: « fann\_get\_cascade\_candidate\_change\_fraction
  - function.fann-get-cascade-candidate-stagnation-epochs.md: fann\_get\_cascade\_candidate\_stagnation\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_candidate\_limit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_candidate\_limit

(PECL fann >= 1.0.0)

fann\_get\_cascade\_candidate\_limit — Повертає межу кандидата

### Опис

```methodsynopsis
fann_get_cascade_candidate_limit(resource $ann): float
```

Межа кандидата - це межа того, скільки нейронів кандидата може бути навчено. Обмеження – це обмеження на співвідношення між MSE та балом кандидата.

Встановлює це більш низьке значення, щоб уникнути переоснащення, і більш високе, якщо переоснащення перестав бути проблемою.

Гранична кількість кандидатів за умовчанням становить 1000.0.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Предел кандидата или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_candidate\_limit()](function.fann-set-cascade-candidate-limit.md) \- встановлює ліміт кандидатів
