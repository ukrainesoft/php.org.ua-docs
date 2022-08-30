Форматує дату/час за Грінвічем

-   [« gettimeofday](function.gettimeofday.md)
    
-   [gmmktime »](function.gmmktime.md)
    
-   [PHP Manual](index.md)
    
-   [Функції дати та часу](ref.datetime.md)
    
-   Форматує дату/час за Грінвічем
    

# gmdate

(PHP 4, PHP 5, PHP 7, PHP 8)

gmdate — Форматує дату/час за Грінвічем

### Опис

```methodsynopsis
gmdate(string $format, ?int $timestamp = null): string
```

Ця функція ідентична функції [date()](function.date.md) за винятком того, що повертає час за Гринвічем (GMT).

### Список параметрів

`format`

Формат дати типу рядок (string). Дивіться параметри форматування для функції [date()](function.date.md)

`timestamp`

Необов'язковий параметр `timestamp` являє собою мітку часу типу int, за умовчанням рівну поточному локальному часу, якщо `timestamp` не вказано або **`null`**. Іншими словами, значення за замовчуванням дорівнює результату функції [time()](function.time.md)

### Значення, що повертаються

Повертає рядок із форматованою датою.

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | `timestamp` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **gmdate()****

Наприклад, у Фінляндії (GMT +0200), перший рядок у наступному прикладі виведе "Jan 01 1998 00:00:00", а другий - "Dec 31 1997 22:00:00".

```php
<?php
echo date("M d Y H:i:s", mktime(0, 0, 0, 1, 1, 1998));
echo gmdate("M d Y H:i:s", mktime(0, 0, 0, 1, 1, 1998));
?>
```

### Дивіться також

-   [date()](function.date.md) - Форматує тимчасову мітку Unix
-   [mktime()](function.mktime.md) - Повертає позначку часу Unix для заданої дати
-   [gmmktime()](function.gmmktime.md) - Повертає локальну мітку часу Unix для часу за Грінвічем
-   [IntlDateFormatter::format()](intldateformatter.format.md) - Форматує значення дати/часу у вигляді рядка