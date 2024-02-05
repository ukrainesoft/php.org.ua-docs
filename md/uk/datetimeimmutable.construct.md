---
navigation:
  - datetimeimmutable.add.md: '« DateTimeImmutable::add'
  - datetimeimmutable.createfromformat.md: 'DateTimeImmutable::createFromFormat »'
  - index.md: PHP Manual
  - class.datetimeimmutable.md: DateTimeImmutable
title: 'DateTimeImmutable::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeImmutable::\_\_construct

# date\_create\_immutable

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::\_\_construct -- date\_create\_immutable — Повертає новий об'єкт DateTimeImmutable

### Опис

Об'єктно-орієнтований стиль

public **DateTimeImmutable::\_\_construct**(string`$datetime` = "now", ?[DateTimeZone](class.datetimezone.md) `$timezone` **`null`**) .

Процедурний стиль

```methodsynopsis
date_create_immutable(string $datetime = "now", ?DateTimeZone $timezone = null): DateTimeImmutable|false
```

Повертає новий об'єкт DateTimeImmutable.

### Список параметрів

`datetime`

Рядок дати/часу. Пояснення коректних форматів наведено в розділі [Формати дати та часу](datetime.formats.md)

Для получения текущего времени в параметр`timezone` можна передати рядок `"now"`

`timezone`

Об'єкт [DateTimeZone](class.datetimezone.md), представляющий часовой пояс параметра`datetime`

Якщо параметр `timezone` опущений або дорівнює **`null`**, буде використано поточний часовий пояс.

> **Зауваження** :
> 
> Параметр`timezone` і поточний часовий пояс буде проігноровано, якщо параметр `datetime` або є тимчасовою міткою UNIX (наприклад, `@946684800`), або вказаний часовий пояс (наприклад, `2010-01-28T15:00:00+02:00`или`2010-07-05T06:00:00Z`

### Значення, що повертаються

Повертає новий екземпляр DateTimeImmutable.

### Помилки

Якщо буде передано рядок з неправильною датою/часом, буде викинуто виняток [DateMalformedStringException](class.datemalformedstringexception.md). До PHP 8.3 викидався виняток [Exception](class.exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер замість винятку [Exception](class.exception.md) викидається виняток [DateMalformedStringException](class.datemalformedstringexception.md), якщо передано неправильний рядок. |
| 7.1.0 | Відтепер мікросекунди заповнюються фактичним значенням. Чи не '00000'. |

### Приклади

**Приклад #1 Приклад використання** DateTimeImmutable::\_\_construct()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
try {
    $date = new DateTimeImmutable('2000-01-01');
} catch (Exception $e) {
    echo $e->getMessage();
    exit(1);
}

echo $date->format('Y-m-d');
?>
```

Процедурний стиль

```php
<?php
$date = date_create('2000-01-01');
if (!$date) {
    $e = date_get_last_errors();
    foreach ($e['errors'] as $error) {
        echo "$error\n";
    }
    exit(1);
}

echo date_format($date, 'Y-m-d');
?>
```

Результат виконання наведених прикладів:

```
2000-01-01
```

**Приклад #2 Тонкощі **DateTimeImmutable::\_\_construct()****

```php
<?php
// Указанная дата/время в часовом поясе вашего компьютера.
$date = new DateTimeImmutable('2000-01-01');
echo $date->format('Y-m-d H:i:sP') . "\n";

// Указанная дата/время в указанном часовом поясе.
$date = new DateTimeImmutable('2000-01-01', new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

// Текущая дата/время в часовом поясе вашего компьютера.
$date = new DateTimeImmutable();
echo $date->format('Y-m-d H:i:sP') . "\n";

// Текущая дата/время в указанном часовом поясе.
$date = new DateTimeImmutable('now', new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

// Использование временной метки UNIX. Обратите внимание, что результат в часовом поясе UTC.
$date = new DateTimeImmutable('@946684800');
echo $date->format('Y-m-d H:i:sP') . "\n";

// Несуществующие значения переворачиваются.
$date = new DateTimeImmutable('2000-02-30');
echo $date->format('Y-m-d H:i:sP') . "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
2000-01-01 00:00:00-05:00
2000-01-01 00:00:00+12:00
2010-04-24 10:24:16-04:00
2010-04-25 02:24:16+12:00
2000-01-01 00:00:00+00:00
2000-03-01 00:00:00-05:00
```

**Приклад #3 Зміна пов'язаного часового поясу**

```php
<?php
$timeZone = new \DateTimeZone('Asia/Tokyo');

$time = new \DateTimeImmutable();
$time = $time->setTimezone($timeZone);

echo $time->format('Y/m/d H:i:s'), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
2022/08/12 23:49:23
```

**Приклад #4 Використання відносного рядка дати/часу**

```php
<?php
$time = new \DateTimeImmutable("-1 year");

echo $time->format('Y/m/d H:i:s'), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
2021/08/12 15:43:51
```
