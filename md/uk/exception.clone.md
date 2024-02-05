---
navigation:
  - exception.tostring.md: '« Exception::\_\_function toString() { [native code] }'
  - class.errorexception.md: ErrorException »
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::\_\_clone'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Exception::\_\_clone

(PHP 5, PHP 7, PHP 8)

Exception::\_\_clone — Клонувати виняток

### Опис

```methodsynopsis
private Exception::__clone(): void
```

Исключения[Exception](class.exception.md) не можуть бути клоновані, а спроба зробити це викине помилку [Error](class.error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Исключения*не* піддаються клонуванню.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Метод**Exception::\_\_clone()** більше не є остаточним (final). |
