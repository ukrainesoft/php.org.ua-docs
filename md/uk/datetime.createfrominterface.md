Повертає новий об'єкт DateTime, створений із переданого об'єкта, що реалізує інтерфейс DateTimeInterface

-   [« DateTime::createFromImmutable](datetime.createfromimmutable.html)
    
-   [DateTime::getLastErrors »](datetime.getlasterrors.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Повертає новий об'єкт DateTime, створений із переданого об'єкта, що реалізує інтерфейс DateTimeInterface
    

# DateTime::createFromInterface

(PHP 8)

DateTime::createFromInterface - Повертає новий об'єкт DateTime, створений з переданого об'єкта, що реалізує інтерфейс DateTimeInterface

### Опис

```methodsynopsis
public static DateTime::createFromInterface(DateTimeInterface $object): DateTime
```

### Список параметрів

`object`

Об'єкт, що реалізує інтерфейс [DateTimeInterface](class.datetimeinterface.html), з якого треба отримати версію, що змінюється. Сам об'єкт не модифікується. На його основі створюється новий об'єкт [DateTime](class.datetime.html), що містить ту ж інформацію про дату, час і часовий пояс.

### Значення, що повертаються

Повертає новий об'єкт [DateTime](class.datetime.html)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");

$mutable = DateTime::createFromInterface($date);

$date = new DateTime("2014-06-20 11:45 Europe/London");
$also_mutable = DateTime::createFromInterface($date);
?>
```