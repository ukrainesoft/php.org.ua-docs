Створює новий об'єкт DateTime

-   [« datecreateimmutable](function.date-create-immutable.html)
    
-   [datedateset »](function.date-date-set.html)
    
-   [PHP Manual](index.html)
    
-   [Функции даты и времени](ref.datetime.html)
    
-   Створює новий об'єкт DateTime
    

# datecreate

(PHP 5> = 5.2.0, PHP 7, PHP 8)

datecreate — Створює новий об'єкт [DateTime](class.datetime.html)

### Опис

```methodsynopsis
date_create(string $datetime = "now", ?DateTimeZone $timezone = null): DateTime|false
```

Це процедурна версія методу [DateTime::construct()](datetime.construct.html)

На відміну від конструктора [DateTime](class.datetime.html), функція повертає **`false`** замість виключення, якщо передано до параметра `datetime` рядок неприпустимий.

### Список параметрів

Дивіться [DateTimeImmutable::construct](datetimeimmutable.construct.html)

### Значення, що повертаються

Повертає новий екземпляр DateTime. Процедурний стиль повертає **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTime::construct()](datetime.construct.html) - Конструктор класу DateTime
-   [DateTimeImmutable::construct()](datetimeimmutable.construct.html) - Повертає новий об'єкт DateTimeImmutable