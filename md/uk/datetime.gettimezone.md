---
navigation:
  - datetime.gettimestamp.md: '« DateTimeInterface::getTimestamp'
  - datetime.wakeup.md: 'DateTime::\_\_wakeup »'
  - index.md: PHP Manual
  - class.datetimeinterface.md: DateTimeInterface
title: 'DateTimeInterface::getTimezone'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeInterface::getTimezone

# DateTimeImmutable::getTimezone

# DateTime::getTimezone

# date\_timezone\_get

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DateTimeInterface::getTimezone -- DateTimeImmutable::getTimezone -- DateTime::getTimezone -- date\_timezone\_get — Повертає часовий пояс щодо поточного значення DateTime

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeInterface::getTimezone(): DateTimeZone|false
```

```methodsynopsis
public DateTimeImmutable::getTimezone(): DateTimeZone|false
```

```methodsynopsis
public DateTime::getTimezone(): DateTimeZone|false
```

Процедурний стиль

```methodsynopsis
date_timezone_get(DateTimeInterface $object): DateTimeZone|false
```

Повертає часовий пояс щодо поточного значення DateTime.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [date\_create()](function.date-create.md)

### Значення, що повертаються

Повертає об'єкт [DateTimeZone](class.datetimezone.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** DateTime::getTimezone()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable(null, new DateTimeZone('Europe/London'));
$tz = $date->getTimezone();
echo $tz->getName();
?>
```

Процедурний стиль

```php
<?php
$date = date_create(null, timezone_open('Europe/London'));
$tz = date_timezone_get($date);
echo timezone_name_get($tz);
?>
```

Результат виконання наведених прикладів:

```
Europe/London
```

### Дивіться також

-   [DateTime::setTimezone()](datetime.settimezone.md) \- Встановлює часовий пояс для об'єкта класу DateTime
