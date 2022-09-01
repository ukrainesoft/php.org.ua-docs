---
navigation:
  - function.fann-clear-scaling-params.html: « fannclearscalingparams
  - function.fann-create-from-file.html: fanncreatefromfile »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncopy
---
# fanncopy

(PECL fann> = 1.0.0)

fanncopy — Створює копію структури fann

### Опис

```methodsynopsis
fann_copy(resource $ann): resource
```

Створює копію структури fann.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

У разі успішного виконання повертає копію ресурсу нейронного ланцюга або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fanntest()](function.fann-test.html) - Тестування з набором вхідних даних та бажаним результатом
