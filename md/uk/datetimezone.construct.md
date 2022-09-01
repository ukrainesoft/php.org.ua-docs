---
navigation:
  - class.datetimezone.md: « DateTimeZone
  - datetimezone.getlocation.md: 'DateTimeZone::getLocation »'
  - index.md: PHP Manual
  - class.datetimezone.md: DateTimeZone
title: 'DateTimeZone::construct'
---
# DateTimeZone::construct

# timezoneopen

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTimeZone::construct - timezoneopen — Створює новий об'єкт DateTimeZone

### Опис

Об'єктно-орієнтований стиль

public **DateTimeZone::construct**(string `$timezone`

Процедурний стиль

```methodsynopsis
timezone_open(string $timezone): DateTimeZone|false
```

Створює новий об'єкт DateTimeZone.

Об'єкт DateTimeZone надає доступ до трьох різних типів правил часових зон: Зміщення UTC (тип `1`), скорочення часового поясу (тип `2`) та [ідентифікатори часових поясів](timezones.md), опубліковані в базі даних часових поясів IANA (тип `3`

Об'єкт DateTimeZone може бути приєднаний до об'єктів [DateTime](class.datetime.md) і [DateTimeImmutable](class.datetimeimmutable.md), щоб мати змогу відображати часовий пояс, розташований у цих об'єктах у локальному часовому поясі.

### Список параметрів

`timezone`

Одне з підтримуваних [імен часових поясів](timezones.md) або значення усунення (+0200) або абревіатура часового поясу (BST).

### Значення, що повертаються

У разі успішного виконання повертає [DateTimeZone](class.datetimezone.md). Процедурний стиль повертає **`false`** у разі виникнення помилки.

### Помилки

Метод викидає виняток [Exception](class.exception.md), якщо цей часовий пояс не розпізнаний як допустимий.

### Приклади

**Приклад #1 Створення та приєднання DateTimeZone до DateTimeImmutable**

```php
<?php
$d = new DateTimeImmutable("2022-06-02 15:44:48 UTC");

$timezones = [ 'Europe/London', 'GMT+04:45', '-06:00', 'CEST' ];

foreach ($timezones as $tz) {
    $tzo = new DateTimeZone($tz);

    $local = $d->setTimezone($tzo);
    echo $local->format(DateTimeInterface::RFC2822 . ' — e'), "\n";
}
?>
```

Результат виконання цього прикладу:

Thu, 02 Jun 2022 16:44:48 +0100 - Europe/London  
Thu, 02 Jun 2022 20:29:48 +0445 - +04:45  
Thu, 02 Jun 2022 09:44:48 -0600 - -06:00  
Thu, 02 Jun 2022 17:44:48 +0200 - CEST

**Приклад #2 Перехоплення помилок під час створення екземпляра [DateTimeZone](class.datetimezone.md)**

```php
<?php
// Обработка ошибок с помощью перехвата исключений
$timezones = array('Europe/London', 'Mars/Phobos', 'Jupiter/Europa');

foreach ($timezones as $tz) {
    try {
        $mars = new DateTimeZone($tz);
    } catch(Exception $e) {
        echo $e->getMessage() . '<br />';
    }
}
?>
```

Результат виконання цього прикладу:

```
DateTimeZone::__construct() [datetimezone.--construct]: Unknown or bad timezone (Mars/Phobos)
DateTimeZone::__construct() [datetimezone.--construct]:  Unknown or bad timezone (Jupiter/Europa)
```
