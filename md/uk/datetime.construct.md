Конструктор класу DateTime

-   [« DateTime::add](datetime.add.html)
    
-   [DateTime::createFromFormat »](datetime.createfromformat.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Конструктор класу DateTime
    

# DateTime::construct

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTime::construct - Конструктор класу DateTime

### Опис

public **DateTime::construct**(string `$datetime` = "now", ?[DateTimeZone](class.datetimezone.html) `$timezone` **`null`**

Подібний до конструктора [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.html), крім роботи з об'єктом [DateTime](class.datetime.html). Замість цього класу розгляньте можливість використання класу [DateTimeImmutable](class.datetimeimmutable.html)

Повертає новий об'єкт DateTime.

### Список параметрів

`datetime`

Рядок дати/часу. Пояснення коректних форматів наведено в розділі [Форматы даты и времени](datetime.formats.html)

Якщо використовується аргумент `$timezone`, то для отримання поточного часу в новому об'єкті достатньо передати `"now"` як цей аргумент.

`timezone`

Об'єкт класу [DateTimeZone](class.datetimezone.html), що представляє часовий пояс параметра `$datetime`

Якщо аргумент `$timezone` не заданий або **`null`**, буде використано поточний часовий пояс.

> **Зауваження**
> 
> Значення аргументу `$timezone`, так само як і поточний часовий пояс не враховуватимуться, якщо як аргумент `$datetime` передається мітка часу UNIX (наприклад, `@946684800`) або час, в якому часовий пояс вже міститься (наприклад, `2010-01-28T15:00:00+02:00`

### Значення, що повертаються

Повертає створений об'єкт класу DateTime. Процедурний стиль повертає **`false`** у разі виникнення помилки.

### Дивіться також

-   [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.html) - Повертає новий об'єкт DateTimeImmutable