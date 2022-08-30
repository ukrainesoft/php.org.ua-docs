Повертає часовий пояс відповідно до абревіатури

-   [« timezonelocationget](function.timezone-location-get.html)
    
-   [timezonenameget »](function.timezone-name-get.html)
    
-   [PHP Manual](index.html)
    
-   [Функции даты и времени](ref.datetime.html)
    
-   Повертає часовий пояс відповідно до абревіатури
    

# timezonenamefromabbr

(PHP 5> = 5.1.3, PHP 7, PHP 8)

timezonenamefromabbr — Повертає часовий пояс відповідно до абревіатури.

### Опис

```methodsynopsis
timezone_name_from_abbr(string $abbr, int $utcOffset = -1, int $isDST = -1): string|false
```

### Список параметрів

`abbr`

Абревіатура часового поясу.

`utcOffset`

Зміщення щодо GMT за секунди. За замовчуванням -1, що означає повернення першого знайденого часового поясу, що відповідає абревіатурі `abbr`. В іншому випадку буде здійснено пошук часового поясу із заданим усуненням. Якщо пошук завершиться невдачею, буде повернено найближчий часовий пояс.

`isDST`

Виправлення на літній час. За замовчуванням -1, у цьому випадку виправлення на літній час не враховується. Якщо передано 1, усунення `utcOffset` враховує літній час, що діє. Якщо заданий 0, `utcOffset` розраховується з урахуванням зимового часу. Якщо `abbr` не існує, визначення часового поясу спирається тільки на `utcOffset` і `isDST`

### Значення, що повертаються

Повертає ім'я часового поясу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **timezonenamefromabbr()****

```php
<?php
echo timezone_name_from_abbr("CET") . "\n";
echo timezone_name_from_abbr("", 3600, 0) . "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Europe/Berlin
Europe/Paris
```

### Дивіться також

-   [timezoneabbreviationslist()](function.timezone-abbreviations-list.html) - Псевдонім DateTimeZone::listAbbreviations