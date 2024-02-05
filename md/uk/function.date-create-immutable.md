---
navigation:
  - function.date-create-immutable-from-format.md: « date\_create\_immutable\_from\_format
  - function.date-create.md: date\_create »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: date\_create\_immutable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# date\_create\_immutable

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

date\_create\_immutable — Створює новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md)

### Опис

```methodsynopsis
date_create_immutable(string $datetime = "now", ?DateTimeZone $timezone = null): DateTimeImmutable|false
```

Аналог метода[DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md) у процедурному стилі.

На відміну від конструктора [DateTimeImmutable](class.datetimeimmutable.md), функція поверне **`false`**, а не викине виняток, якщо переданий у конструктор рядок `datetime`указана некорректно.

### Список параметрів

Смотрите[DateTimeImmutable::\_\_construct](datetimeimmutable.construct.md)

### Значення, що повертаються

Повертає новий екземпляр DateTimeImmutable. або \*\*`false`\*\*в случае возникновения ошибки

### Дивіться також

-   [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md) \- Розбирає рядок з датою згідно з вказаним форматом
