Отримує локаль засобу форматування

-   [« NumberFormatter::getErrorMessage](numberformatter.geterrormessage.html)
    
-   [NumberFormatter::getPattern »](numberformatter.getpattern.html)
    
-   [PHP Manual](index.html)
    
-   [NumberFormatter](class.numberformatter.html)
    
-   Отримує локаль засобу форматування
    

# NumberFormatter::getLocale

# numfmtgetlocale

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::getLocale -- numfmtgetlocale — Отримує локаль засобу форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::getLocale(int $type = ULOC_ACTUAL_LOCALE): string|false
```

Процедурний стиль

```methodsynopsis
numfmt_get_locale(NumberFormatter $formatter, int $type = ULOC_ACTUAL_LOCALE): string|false
```

Отримує назву локалі засобу форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.html)

`type`

Ви можете вибрати дійсну або фактичну локаль ( **`Locale::VALID_LOCALE`** \*\*`Locale::ACTUAL_LOCALE`\*\*відповідно). За промовчанням використовується фактична локаль.

### Значення, що повертаються

Ім'я локалі, що використовується для створення засобу форматування або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmtgetlocale()****

```php
<?php
$req     = 'fr_FR_PARIS';
$fmt     = numfmt_create( $req,  NumberFormatter::DECIMAL);
$res_val = numfmt_get_locale( $fmt, Locale::VALID_LOCALE );
$res_act = numfmt_get_locale( $fmt, Locale::ACTUAL_LOCALE );
printf( "Запрошенная локаль: %s\nДействительная локаль: %s\nФактическая локаль: %s\n",
         $req, $res_val, $res_act );
?>
```

Результат виконання цього прикладу:

```
Запрошенная локаль: fr_FR_PARIS
Действительная локаль: fr_FR
Фактическая локаль: fr
```

### Дивіться також

-   [numfmtcreate()](numberformatter.create.html) - Створює засіб форматування чисел
-   [numfmtgeterrorcode()](numberformatter.geterrorcode.html) - Отримує останній код помилки засобу форматування