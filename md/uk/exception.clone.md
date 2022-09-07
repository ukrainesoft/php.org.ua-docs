---
navigation:
  - exception.tostring.md: '« Exception::toString'
  - class.errorexception.md: ErrorException »
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::clone'
---
# Exception::clone

(PHP 5, PHP 7, PHP 8)

Exception::clone — Клонувати виняток

### Опис

```methodsynopsis
private Exception::__clone(): void
```

Намагається клонувати виняток, що призводить до фатальної помилки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Винятки *не* піддаються клонуванню.

### список змін

| Версия | Описание |
| --- | --- |
|  | Метод **Exception::clone()** більше не є остаточним (final). |
