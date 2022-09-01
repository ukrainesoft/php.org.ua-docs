---
navigation:
  - datetime.format.md: '« DateTimeInterface::format'
  - datetime.gettimestamp.md: 'DateTimeInterface::getTimestamp »'
  - index.md: PHP Manual
  - class.datetimeinterface.md: DateTimeInterface
title: 'DateTimeInterface::getOffset'
---
# DateTimeInterface::getOffset

# DateTimeImmutable::getOffset

# DateTime::getOffset

# dateoffsetget

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTimeInterface::getOffset -- DateTimeImmutable::getOffset -- DateTime::getOffset -- dateoffsetget — Повертає зсув часового поясу

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

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [datecreate()](function.date-create.html)

### Значення, що повертаються

У разі успішного виконання повертає зміщення часового поясу щодо UTC за секунди.

### список змін

| Версия | Описание |
| --- | --- |
|  | До цієї версії, у разі виникнення помилки поверталося **`false`** |

### Приклади

**Приклад #1 Приклад використання **DateTime::getOffset()****

Об'єктно-орієнтований стиль

```php
<?php
$winter = new DateTimeImmutable('2010-12-21', new DateTimeZone('America/New_York'));
$summer = new DateTimeImmutable('2008-06-21', new DateTimeZone('America/New_York'));

echo $winter->getOffset() . "\n";
echo $summer->getOffset() . "\n";
?>
```

Процедурний стиль

```php
<?php
$winter = date_create('2010-12-21', timezone_open('America/New_York'));
$summer = date_create('2008-06-21', timezone_open('America/New_York'));

echo date_offset_get($winter) . "\n";
echo date_offset_get($summer) . "\n";
?>
```

Результат виконання даних прикладів:

```
-18000
-14400
```

Примітка: -18000 = -5 годин, -14400 = -4 годин.
