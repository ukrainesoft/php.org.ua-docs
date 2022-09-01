---
navigation:
  - function.fann-get-cascade-max-out-epochs.html: « fanngetcascademaxoutepochs
  - function.fann-get-cascade-min-out-epochs.html: fanngetcascademinoutepochs »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetcascademincandepochs
---
# fanngetcascademincandepochs

(PECL fann> = 1.0.0)

fanngetcascademincandepochs - Отримує найменший період кандидата

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

Мінімальний період кандидата або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fannsetcascademincandepochs()](function.fann-set-cascade-min-cand-epochs.md) - встановлює найменший період кандидата
