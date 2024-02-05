---
navigation:
  - datetime.getoffset.md: '« DateTimeInterface::getOffset'
  - datetime.gettimezone.md: 'DateTimeInterface::getTimezone »'
  - index.md: PHP Manual
  - class.datetimeinterface.md: DateTimeInterface
title: 'DateTimeInterface::getTimestamp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeInterface::getTimestamp

# DateTimeImmutable::getTimestamp

# DateTime::getTimestamp

# date\_timestamp\_get

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateTimeInterface::getTimestamp -- DateTimeImmutable::getTimestamp -- DateTime::getTimestamp -- date\_timestamp\_get — Повертає тимчасову мітку Unix

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

Якщо не вийде представити тимчасову мітку цілим числом (int), буде викинуто виняток [DateRangeError](class.daterangeerror.md). До PHP 8.3.0 викидався виняток [ValueError](class.valueerror.md). А до PHP 8.0.0 поверталося логічне значення **`false`**. При цьому мітку часу можна отримати у вигляді рядка (string), викликавши метод [DateTimeInterface::format()](datetime.format.md) з параметром форматування `U`

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер при виході за межі діапазону буде викинуто виняток [DateRangeError](class.daterangeerror.md) |
| 8.0.0 | Функції більше не повертають значення \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Пример #1 Пример использования**DateTime::getTimestamp()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable();
echo $date->getTimestamp();
?>
```

Процедурний стиль

```php
<?php
$date = date_create();
echo date_timestamp_get($date);
?>
```

Висновок наведених прикладів буде схожим на:

```
1272509157
```

Якщо потрібно отримати мітку часу з мілісекундами або мікросекундами, можна використовувати функцію [DateTimeInterface::format()](datetime.format.md)

**Приклад #2 Отримання мітки часу з мілі- та мікросекундами**

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable();
$milli = (int)$date->format('Uv'); // Метка времени с миллисекундами
$micro = (int)$date->format('Uu'); // Метка времени с микросекундами

echo $milli, "\n", $micro, "\n";
?>
```

Висновок наведених прикладів буде схожим на:

```
1674057635586
1674057635586918
```

### Дивіться також

-   [DateTime::setTimestamp()](datetime.settimestamp.md) \- Встановлює дату та час на основі мітки часу Unix
-   [DateTimeImmutable::setTimestamp()](datetimeimmutable.settimestamp.md) \- Встановлює дату та час на основі мітки часу Unix
-   [DateTimeInterface::format()](datetime.format.md) \- Повертає дату, відформатовану згідно з переданим форматом
