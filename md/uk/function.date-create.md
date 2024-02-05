---
navigation:
  - function.date-create-immutable.md: « date\_create\_immutable
  - function.date-date-set.md: date\_date\_set »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: date\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# date\_create

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

date\_create — Створює новий об'єкт [DateTime](class.datetime.md)

### Опис

```methodsynopsis
date_create(string $datetime = "now", ?DateTimeZone $timezone = null): DateTime|false
```

Це процедурна версія методу [DateTime::\_\_construct()](datetime.construct.md)

На відміну від конструктора [DateTime](class.datetime.md), функція повертає **`false`** замість виключення, якщо передано до параметра `datetime`строка недопустима.

### Список параметрів

Смотрите[DateTimeImmutable::\_\_construct](datetimeimmutable.construct.md)

### Значення, що повертаються

Повертає новий екземпляр DateTime. або \*\*`false`\*\*в случае возникновения ошибки

### Дивіться також

-   [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md) \- Повертає новий об'єкт DateTimeImmutable
-   [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md) \- Розбирає рядок з датою згідно з вказаним форматом
-   [DateTime::\_\_construct()](datetime.construct.md) \- Конструктор класу DateTime
