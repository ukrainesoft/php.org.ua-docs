---
navigation:
  - datetime.getlasterrors.md: '« DateTime::getLastErrors'
  - datetime.set-state.md: 'DateTime::\_\_set\_state »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::modify'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::modify

# date\_modify

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DateTime::modify -- date\_modify - Зміна тимчасової мітки

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::modify(string $modifier): DateTime|false
```

Процедурний стиль

```methodsynopsis
date_modify(DateTime $object, string $modifier): DateTime|false
```

Змінює мітку часу об'єкта DateTime шляхом додавання або віднімання часу у форматі, прийнятому для функції [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md)

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [date\_create()](function.date-create.md). Функція змінює цей об'єкт.

`modifier`

Рядок дати/часу. Пояснення коректних форматів наведено в розділі [Формати дати та часу](datetime.formats.md)

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md)для применения в цепи методов или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Тільки для об'єктно-орієнтованого API: Якщо передано рядок з неприпустимою датою/часом, буде викинуто виняток [DateMalformedStringException](class.datemalformedstringexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер замість попередження у методі **DateTime::modify()** викидається виняток [DateMalformedStringException](class.datemalformedstringexception.md), якщо передано неприпустимий рядок. Функція [date\_modify()](function.date-modify.md) не було змінено. |

### Приклади

**Пример #1 Пример использования**DateTime::modify()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTime('2006-12-12');
$date->modify('+1 day');
echo $date->format('Y-m-d');
?>
```

Процедурний стиль

```php
<?php
$date = date_create('2006-12-12');
date_modify($date, '+1 day');
echo date_format($date, 'Y-m-d');
?>
```

Результат виконання наведених прикладів:

```
2006-12-13
```

**Приклад #2 Будьте обережні при додаванні та відніманні місяців**

```php
<?php
$date = new DateTime('2000-12-31');

$date->modify('+1 month');
echo $date->format('Y-m-d') . "\n";

$date->modify('+1 month');
echo $date->format('Y-m-d') . "\n";
?>
```

Результат виконання наведеного прикладу:

```
2001-01-31
2001-03-03
```

**Приклад #3 Підтримуються всі формати дати та часу**

```php
<?php
$date = new DateTime('2020-12-31');

$date->modify('July 1st, 2023');
echo $date->format('Y-m-d H:i') . "\n";

$date->modify('Monday next week');
echo $date->format('Y-m-d H:i') . "\n";

$date->modify('17:30');
echo $date->format('Y-m-d H:i') . "\n";
?>
```

Результат виконання наведеного прикладу:

```
2023-07-01 00:00
2023-07-03 00:00
2023-07-03 17:30
```

### Дивіться також

-   [strtotime()](function.strtotime.md) \- Перетворює текстове подання дати англійською мовою на мітку часу Unix
-   [DateTimeImmutable::modify()](datetimeimmutable.modify.md) \- Створює новий об'єкт із зміненою тимчасовою міткою
-   [DateTime::add()](datetime.add.md) \- Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTime::sub()](datetime.sub.md) \- Віднімає дні, місяці, роки, години, хвилини та секунди з об'єкта DateTime
-   [DateTime::setDate()](datetime.setdate.md) \- Встановлює дату
-   [DateTime::setISODate()](datetime.setisodate.md) \- Встановлює дату у форматі ISO
-   [DateTime::setTime()](datetime.settime.md) \- Встановлює час
-   [DateTime::setTimestamp()](datetime.settimestamp.md) \- Встановлює дату та час на основі мітки часу Unix
