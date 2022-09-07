---
navigation:
  - datetime.createfrominterface.md: '« DateTime::createFromInterface'
  - datetime.modify.md: 'DateTime::modify »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::getLastErrors'
---
# DateTime::getLastErrors

# dategetlasterrors

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::getLastErrors -- dategetlasterrors — Повертає попередження та помилки

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static DateTime::getLastErrors(): array|false
```

Процедурний стиль

```methodsynopsis
date_get_last_errors(): array|false
```

Подібний до методу [DateTimeImmutable::getLastErrors()](datetimeimmutable.getlasterrors.md), крім роботи з об'єктом [DateTime](class.datetime.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив містить інформацію про помилки та попередження або **`false`**, якщо немає ні попереджень, ні помилок.

### Дивіться також

-   [DateTimeImmutable::getLastErrors()](datetimeimmutable.getlasterrors.md) - Повертає попередження та помилки
