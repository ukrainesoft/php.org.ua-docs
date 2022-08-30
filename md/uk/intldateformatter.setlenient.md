Встановлює м'який режим аналізатора

-   [« IntlDateFormatter::setCalendar](intldateformatter.setcalendar.html)
    
-   [IntlDateFormatter::setPattern »](intldateformatter.setpattern.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Встановлює м'який режим аналізатора
    

# IntlDateFormatter::setLenient

# datefmtsetlenient

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::setLenient -- datefmtsetlenient — Встановлює м'який режим аналізатора

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::setLenient(bool $lenient): void
```

Процедурний стиль

```methodsynopsis
datefmt_set_lenient(IntlDateFormatter $formatter, bool $lenient): void
```

Визначає, чи є режим аналізатора строгим чи м'яким при інтерпретації вхідних даних, які точно не відповідають шаблону. Увімкнення м'якого синтаксичного аналізу дозволяє синтаксичному аналізатору приймати помилкові шаблони дати або часу, аналізуючи якнайбільше для отримання значення. Зайва пропуск, нерозпізнані токени або неприпустимі значення ("February 30th") не приймаються.

### Список параметрів

`formatter`

Ресурс засобу форматування.

`lenient`

Встановлює, чи аналізатор vzurbv чи ні, за замовчуванням **`true`** (м'який).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtsetlenient()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'dd/MM/yyyy'
);
echo 'Мягкий режим средства форматирования : ';
if ($fmt->isLenient()) {
    echo 'ДА';
} else {
    echo 'НЕТ';
}
datefmt_parse($fmt, '35/13/1971');
echo "\nПопытка разобрать '35/13/1971'.\nРезультат : " . datefmt_parse($fmt, '35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nСообщение об ошибке : " . intl_get_error_message();
    echo "\nКод ошибки : " . intl_get_error_code();
}
datefmt_set_lenient($fmt, false);
echo "\nТеперь мягкий режим средства форматирования : ";
if ($fmt->isLenient()) {
    echo 'ДА';
} else {
    echo 'НЕТ';
}
datefmt_parse($fmt, '35/13/1971');
echo "\nПопытка разобрать '35/13/1971'.\nРезультат : " . datefmt_parse($fmt, '35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nСообщение об ошибке : ".intl_get_error_message();
    echo "\nКод ошибки : ".intl_get_error_code();
}

?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'dd/MM/yyyy'
);
echo 'Мягкий режим средства форматирования : ';
if ($fmt->isLenient()) {
    echo 'ДА';
} else {
    echo 'НЕТ';
}
$fmt->parse('35/13/1971');
echo "\nПопытка разобрать '35/13/1971'.\nРезультат : " . $fmt->parse('35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nСообщение об ошибке : " . intl_get_error_message();
    echo "\nКод ошибки : " . intl_get_error_code();
}

$fmt->setLenient(FALSE);
echo "\nТеперь мягкий режим средства форматирования : ";
if ($fmt->isLenient()) {
    echo 'ДА';
} else {
    echo 'НЕТ';
}
$fmt->parse('35/13/1971');
echo "\nПопытка разобрать '35/13/1971'.\nРезультат : " . $fmt->parse('35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nСообщение об ошибке : " . intl_get_error_message();
    echo "\nКод ошибки : " . intl_get_error_code();
}

?>
```

Результат виконання цього прикладу:

```
Мягкий режим средства форматирования : ДА
Попытка разобрать '35/13/1971'.
Результат : 66038400
Теперь мягкий режим средства форматирования : НЕТ
Попытка разобрать '35/13/1971'.
Результат :
Сообщение об ошибке : Date parsing failed: U_PARSE_ERROR
Код ошибки : 9
```

### Дивіться також

-   [datefmtісlenient()](intldateformatter.islenient.html) - Отримує поблажливість, що використовується для IntlDateFormatter
-   [datefmtcreate()](intldateformatter.create.html) - Створює засіб форматування дати