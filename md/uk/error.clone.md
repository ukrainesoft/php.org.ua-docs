---
navigation:
  - error.tostring.md: '« Error::\_\_function toString() { [native code] }'
  - class.argumentcounterror.md: ArgumentCountError »
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::\_\_clone'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::\_\_clone

(PHP 7, PHP 8)

Error::\_\_clone - Клонує помилку

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

| Версия | Опис |
| --- | --- |
| 8.1.0 | Метод**Error::\_\_clone()** більше не є остаточним (final). |
