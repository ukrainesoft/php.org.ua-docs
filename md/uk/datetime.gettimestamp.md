---
navigation:
  - datetime.getoffset.md: '« DateTimeInterface::getOffset'
  - datetime.gettimezone.md: 'DateTimeInterface::getTimezone »'
  - index.md: PHP Manual
  - class.datetimeinterface.md: DateTimeInterface
title: 'DateTimeInterface::getTimestamp'
---
# DateTimeInterface::getTimestamp

# DateTimeImmutable::getTimestamp

# DateTime::getTimestamp

# datetimestampget

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTimeInterface::getTimestamp -- DateTimeImmutable::getTimestamp -- DateTime::getTimestamp -- datetimestampget — Повертає тимчасову мітку Unix

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeInterface::getTimestamp(): int
```

```methodsynopsis
public DateTimeImmutable::getTimestamp(): int
```

```methodsynopsis
public DateTime::getTimestamp(): int
```

Процедурний стиль

```methodsynopsis
date_timestamp_get(DateTimeInterface $object): int
```

Повертає тимчасову мітку Unix.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тимчасову мітку Unix для цієї дати.

### Помилки

Якщо тимчасова мітка не може бути представлена ​​як ціле число (int), викидається [ValueError](class.valueerror.md). До PHP 8.0.0 у цьому випадку поверталося **`false`**. Тим не менш, мітку часу можна отримати як рядок (string) за допомогою [DateTimeInterface::format()](datetime.format.md) з форматом `U`

### список змін

| Версия | Описание |
| --- | --- |
|  | Функції більше не повертають **`false`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Приклад використання **DateTime::getTimestamp()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable();
echo $date->getTimestamp();
?>
```

Процедурний стиль

```php
<?php
$date = date_create();
echo date_timestamp_get($date);
?>
```

Результатом виконання даних прикладів буде щось подібне:

```
1272509157
```

### Дивіться також

-   [DateTime::setTimestamp()](datetime.settimestamp.md) - Встановлює дату та час на основі мітки часу Unix
-   [DateTime::format()](datetime.format.md) - Повертає дату, відформатовану згідно з переданим форматом
