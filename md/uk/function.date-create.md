---
navigation:
  - function.date-create-immutable.md: « datecreateimmutable
  - function.date-date-set.md: datedateset »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: datecreate
---
# datecreate

(PHP 5> = 5.2.0, PHP 7, PHP 8)

datecreate — Створює новий об'єкт [DateTime](class.datetime.md)

### Опис

```methodsynopsis
date_create(string $datetime = "now", ?DateTimeZone $timezone = null): DateTime|false
```

Це процедурна версія методу [DateTime::construct()](datetime.construct.md)

На відміну від конструктора [DateTime](class.datetime.md), функція повертає **`false`** замість виключення, якщо передано до параметра `datetime` рядок неприпустимий.

### Список параметрів

Дивіться [DateTimeImmutable::construct](datetimeimmutable.construct.md)

### Значення, що повертаються

Повертає новий екземпляр DateTime. Процедурний стиль повертає **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTime::construct()](datetime.construct.md) - Конструктор класу DateTime
-   [DateTimeImmutable::construct()](datetimeimmutable.construct.md) - Повертає новий об'єкт DateTimeImmutable
