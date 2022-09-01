---
navigation:
  - datetime.getlasterrors.md: '« DateTime::getLastErrors'
  - datetime.set-state.html: 'DateTime::setstate »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::modify'
---
# DateTime::modify

# datemodify

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTime::modify -- datemodify - Зміна тимчасової мітки

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTime::modify(string $modifier): DateTime|false
```

Процедурний стиль

```methodsynopsis
date_modify(DateTime $object, string $modifier): DateTime|false
```

Змінює мітку часу об'єкта DateTime шляхом додавання або віднімання часу у форматі, прийнятому для функції [DateTimeImmutable::construct()](datetimeimmutable.construct.md)

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [datecreate()](function.date-create.html). Функція змінює цей об'єкт.

`modifier`

Рядок дати/часу. Пояснення коректних форматів наведено в розділі [Формати дати та часу](datetime.formats.md)

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.md) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DateTime::modify()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTime('2006-12-12');
$date->modify('+1 day');
echo $date->format('Y-m-d');
?>
```

Процедурний стиль

```php
<?php
$date = date_create('2006-12-12');
date_modify($date, '+1 day');
echo date_format($date, 'Y-m-d');
?>
```

Результат виконання даних прикладів:

```
2006-12-13
```

**Приклад #2 Будьте обережні при додаванні та відніманні місяців**

```php
<?php
$date = new DateTime('2000-12-31');

$date->modify('+1 month');
echo $date->format('Y-m-d') . "\n";

$date->modify('+1 month');
echo $date->format('Y-m-d') . "\n";
?>
```

Результат виконання цього прикладу:

```
2001-01-31
2001-03-03
```

### Дивіться також

-   [strtotime()](function.strtotime.md) - Перетворює текстове подання дати англійською мовою на позначку часу Unix
-   [DateTimeImmutable::modify()](datetimeimmutable.modify.md) - Створює новий об'єкт із зміненою тимчасовою міткою
-   [DateTime::add()](datetime.add.md) - Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTime::sub()](datetime.sub.md) - Змінює вказаний об'єкт DateTime, віднімаючи вказаний об'єкт DateInterval.
-   [DateTime::setDate()](datetime.setdate.md) - Встановлює дату
-   [DateTime::setISODate()](datetime.setisodate.md) - Встановлює дату у форматі ISO
-   [DateTime::setTime()](datetime.settime.md) - Встановлює час
-   [DateTime::setTimestamp()](datetime.settimestamp.md) - Встановлює дату та час на основі мітки часу Unix
