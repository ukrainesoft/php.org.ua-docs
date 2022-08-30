Зміна тимчасової мітки

-   [« DateTime::getLastErrors](datetime.getlasterrors.html)
    
-   [DateTime::setstate »](datetime.set-state.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Зміна тимчасової мітки
    

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

Змінює мітку часу об'єкта DateTime шляхом додавання або віднімання часу у форматі, прийнятому для функції [DateTimeImmutable::construct()](datetimeimmutable.construct.html)

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.html), що повертається [datecreate()](function.date-create.html). Функція змінює цей об'єкт.

`modifier`

Рядок дати/часу. Пояснення коректних форматів наведено в розділі [Форматы даты и времени](datetime.formats.html)

### Значення, що повертаються

Повертає модифікований об'єкт [DateTime](class.datetime.html) для застосування в ланцюгу методів або **`false`** у разі виникнення помилки.

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

-   [strtotime()](function.strtotime.html) - Перетворює текстове подання дати англійською мовою на позначку часу Unix
-   [DateTimeImmutable::modify()](datetimeimmutable.modify.html) - Створює новий об'єкт із зміненою тимчасовою міткою
-   [DateTime::add()](datetime.add.html) - Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTime::sub()](datetime.sub.html) - Змінює вказаний об'єкт DateTime, віднімаючи вказаний об'єкт DateInterval.
-   [DateTime::setDate()](datetime.setdate.html) - Встановлює дату
-   [DateTime::setISODate()](datetime.setisodate.html) - Встановлює дату у форматі ISO
-   [DateTime::setTime()](datetime.settime.html) - Встановлює час
-   [DateTime::setTimestamp()](datetime.settimestamp.html) - Встановлює дату та час на основі мітки часу Unix