---
navigation:
  - datetime.format.md: '« DateTimeInterface::format'
  - datetime.gettimestamp.md: 'DateTimeInterface::getTimestamp »'
  - index.md: PHP Manual
  - class.datetimeinterface.md: DateTimeInterface
title: 'DateTimeInterface::getOffset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeInterface::getOffset

# DateTimeImmutable::getOffset

# DateTime::getOffset

# date\_offset\_get

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DateTimeInterface::getOffset -- DateTimeImmutable::getOffset -- DateTime::getOffset -- date\_offset\_get — Повертає зсув часового поясу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeInterface::getOffset(): int
```

```methodsynopsis
public DateTimeImmutable::getOffset(): int
```

```methodsynopsis
public DateTime::getOffset(): int
```

Процедурний стиль

```methodsynopsis
date_offset_get(DateTimeInterface $object): int
```

Повертає усунення часового поясу.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [date\_create()](function.date-create.md)

### Значення, що повертаються

У разі успішного виконання повертає зміщення часового поясу щодо UTC за секунди.

### Приклади

**Приклад #1 Приклад використання** DateTime::getOffset()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$winter = new DateTimeImmutable('2010-12-21', new DateTimeZone('America/New_York'));
$summer = new DateTimeImmutable('2008-06-21', new DateTimeZone('America/New_York'));

echo $winter->getOffset() . "\n";
echo $summer->getOffset() . "\n";
?>
```

Процедурний стиль

```php
<?php
$winter = date_create('2010-12-21', timezone_open('America/New_York'));
$summer = date_create('2008-06-21', timezone_open('America/New_York'));

echo date_offset_get($winter) . "\n";
echo date_offset_get($summer) . "\n";
?>
```

Результат виконання наведених прикладів:

```
-18000
-14400
```

Примітка: -18000 = -5 годин, -14400 = -4 годин.
