---
navigation:
  - function.fann-get-cascade-max-out-epochs.md: « fann\_get\_cascade\_max\_out\_epochs
  - function.fann-get-cascade-min-out-epochs.md: fann\_get\_cascade\_min\_out\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_min\_cand\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_min\_cand\_epochs

(PECL fann >= 1.0.0)

fann\_get\_cascade\_min\_cand\_epochs - Отримує найменший період кандидата

### Опис

```methodsynopsis
fann_get_cascade_min_cand_epochs(resource $ann): int
```

Мінімальний період кандидата визначає мінімальну кількість періодів, у яких вхідні з'єднання з кандидатами можуть бути навчені перед додаванням нового нейрона-кандидата.

Мінімальний період кандидата за замовчуванням – 50.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Мінімальний період кандидата або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_cascade\_min\_cand\_epochs()](function.fann-set-cascade-min-cand-epochs.md) \- встановлює найменший період кандидата
