---
navigation:
  - error.tostring.md: '« Error::toString'
  - class.argumentcounterror.md: ArgumentCountError »
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::clone'
---
# Error::clone

(PHP 7, PHP 8)

Error::clone - Клонує помилку

### Опис

```methodsynopsis
private Error::__clone(): void
```

Об'єкт класу Error не можна клонувати, тому ця функція викликає фатальну помилку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Об'єкт класу Error *не можна* клонувати.

### список змін

| Версия | Описание |
| --- | --- |
|  | Метод **Error::clone()** більше не є остаточним (final). |
