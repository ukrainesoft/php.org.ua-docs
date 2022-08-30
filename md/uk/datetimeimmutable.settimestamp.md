Встановлює дату та час на основі мітки часу Unix

-   [« DateTimeImmutable::setTime](datetimeimmutable.settime.md)
    
-   [DateTimeImmutable::setTimezone »](datetimeimmutable.settimezone.md)
    
-   [PHP Manual](index.md)
    
-   [DateTimeImmutable](class.datetimeimmutable.md)
    
-   Встановлює дату та час на основі мітки часу Unix
    

# DateTimeImmutable::setTimestamp

(PHP 5> = 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::setTimestamp — Встановлює дату та час на основі мітки часу Unix

### Опис

```methodsynopsis
public DateTimeImmutable::setTimestamp(int $timestamp): DateTimeImmutable
```

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md), побудований зі старого, з датою та часом, встановленими на основі мітки часу Unix.

### Список параметрів

`timestamp`

Мітка часу Unix представляє дату. Встановлення міток часу поза діапазоном цілого числа (int) можливе при використанні методу [DateTimeImmutable::modify()](datetimeimmutable.modify.md) з форматом `@`

### Значення, що повертаються

Повертає новий об'єкт [DateTimeImmutable](class.datetimeimmutable.md) з модифікованими даними або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DateTimeImmutable::setTimestamp()****

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable();
echo $date->format('U = Y-m-d H:i:s') . "\n";

$newDate = $date->setTimestamp(1171502725);
echo $newDate->format('U = Y-m-d H:i:s') . "\n";
?>
```

Результатом виконання даних прикладів буде щось подібне:

```
1272508903 = 2010-04-28 22:41:43
1171502725 = 2007-02-14 20:25:25
```

### Дивіться також

-   [DateTimeImmutable::getTimestamp()](datetime.gettimestamp.md) - Повертає тимчасову мітку Unix