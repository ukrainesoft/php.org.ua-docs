---
navigation:
  - function.fann-clear-scaling-params.md: « fann\_clear\_scaling\_params
  - function.fann-create-from-file.md: fann\_create\_from\_file »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_copy

(PECL fann >= 1.0.0)

fann\_copy — Створює копію структури fann

### Опис

```methodsynopsis
fann_copy(resource $ann): resource
```

Створює копію структури fann.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

У разі успішного виконання повертає копію ресурсу нейронного ланцюга або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_test()](function.fann-test.md) \- Тестування з набором вхідних даних та бажаним результатом
