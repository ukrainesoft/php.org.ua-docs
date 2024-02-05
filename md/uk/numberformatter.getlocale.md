---
navigation:
  - numberformatter.geterrormessage.md: '« NumberFormatter::getErrorMessage'
  - numberformatter.getpattern.md: 'NumberFormatter::getPattern »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::getLocale'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::getLocale

# numfmt\_get\_locale

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::getLocale -- numfmt\_get\_locale — Отримує локаль засобу форматування

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

Об'єкт [NumberFormatter](class.numberformatter.md)

`type`

Ви можете вибрати дійсну або фактичну локаль ( **`Locale::VALID_LOCALE`** \*\*`Locale::ACTUAL_LOCALE`\*\*відповідно). За промовчанням використовується фактична локаль.

### Значення, що повертаються

Имя локали, используемое для создания средства форматирования или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** numfmt\_get\_locale()\*\*\*\*

```php
<?php
$req     = 'fr_FR_PARIS';
$fmt     = numfmt_create( $req,  NumberFormatter::DECIMAL);
$res_val = numfmt_get_locale( $fmt, Locale::VALID_LOCALE );
$res_act = numfmt_get_locale( $fmt, Locale::ACTUAL_LOCALE );
printf( "Запрошенная локаль: %s\nДействительная локаль: %s\nФактическая локаль: %s\n",
         $req, $res_val, $res_act );
?>
```

Результат виконання наведеного прикладу:

```
Запрошенная локаль: fr_FR_PARIS
Действительная локаль: fr_FR
Фактическая локаль: fr
```

### Дивіться також

-   [numfmt\_create()](numberformatter.create.md) \- Створює засіб форматування чисел
-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.md) \- Отримує останній код помилки засобу форматування
