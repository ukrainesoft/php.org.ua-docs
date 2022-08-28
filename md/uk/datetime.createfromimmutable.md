Повертає об'єкт DateTime інкапсулюючий заданий об'єкт DateTimeImmutable

-   [« DateTime::createFromFormat](datetime.createfromformat.html)
    
-   [DateTime::createFromInterface »](datetime.createfrominterface.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Повертає об'єкт DateTime інкапсулюючий заданий об'єкт DateTimeImmutable
    

# DateTime::createFromImmutable

(PHP 7> = 7.3.0, PHP 8)

DateTime::createFromImmutable — Повертає об'єкт DateTime інкапсулюючий заданий об'єкт DateTimeImmutable

### Опис

```methodsynopsis
public static DateTime::createFromImmutable(DateTimeImmutable $object): DateTime
```

### Список параметрів

`object`

Незмінний об'єкт [DateTimeImmutable](class.datetimeimmutable.html), який потребує перетворення на змінну форму. Сам об'єкт не змінюється, а натомість створюється новий об'єкт класу [DateTime](class.datetime.html), що містить самі дані: дату, час і часовий пояс.

### Значення, що повертаються

Повертає новий об'єкт класу [DateTime](class.datetime.html)

### Приклади

**Приклад #1 Створення об'єкта, що змінюється**

```php
<?php
$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");

$mutable = DateTime::createFromImmutable( $date );
?>
```