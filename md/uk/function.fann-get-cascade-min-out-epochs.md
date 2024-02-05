---
navigation:
  - function.fann-get-cascade-min-cand-epochs.md: « fann\_get\_cascade\_min\_cand\_epochs
  - function.fann-get-cascade-num-candidate-groups.md: fann\_get\_cascade\_num\_candidate\_groups »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_min\_out\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_min\_out\_epochs

(PECL fann >= 1.0.0)

fann\_get\_cascade\_min\_out\_epochs — Повертає мінімальну кількість періодів

### Опис

```methodsynopsis
fann_get_cascade_min_out_epochs(resource $ann): int
```

Мінімальна кількість періодів визначає кількість періодів, у яких вихідні з'єднання мають бути навчені після додавання нового нейрона-кандидата.

Мінімальна кількість періодів за замовчуванням – 50.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Минимальное количество периодов или\*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_cascade\_min\_out\_epochs()](function.fann-set-cascade-min-out-epochs.md) \- Встановлює мінімальні епохи вихідних даних
