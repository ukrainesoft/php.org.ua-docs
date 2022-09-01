---
navigation:
  - intldateformatter.gettimezone.html: '« IntlDateFormatter::getTimeZone'
  - intldateformatter.localtime.html: 'IntlDateFormatter::localtime »'
  - index.html: PHP Manual
  - class.intldateformatter.html: IntlDateFormatter
title: 'IntlDateFormatter::isLenient'
---
# IntlDateFormatter::isLenient

# datefmtісlenient

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::isLenient -- datefmtісlenient — Отримує поблажливість для IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::isLenient(): bool
```

Процедурний стиль

```methodsynopsis
datefmt_is_lenient(IntlDateFormatter $formatter): bool
```

Перевіряє, чи є синтаксичний аналізатор суворим чи поблажливим при інтерпретації вхідних даних, які не відповідають шаблону.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо парсер поблажливий або \*\*`false`\*\*якщо парсер строгий. За промовчанням парсер поблажливий.

### Приклади

**Приклад #1 Приклад використання **datefmtісlenient()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'dd/mm/yyyy'
);
echo 'Снисходительность средства форматирования: ';
if ($fmt->isLenient()) {
    echo 'Да';
} else {
    echo 'Нет';
}
datefmt_parse($fmt, '35/13/1971');
echo "\n Попытка выполнить синтаксический анализ '35/13/1971'.\nРезультат: " . datefmt_parse($fmt, '35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nОшибка: " . intl_get_error_message();
    echo "\nКод ошибки: " . intl_get_error_code();
}
datefmt_set_lenient($fmt,false);
echo 'Теперь снисходительность средства форматирования: ';
if ($fmt->isLenient()) {
    echo 'Да';
} else {
    echo 'Нет';
}
datefmt_parse($fmt, '35/13/1971');
echo "\n Попытка выполнить синтаксический анализ '35/13/1971'.\nРезультат: " . datefmt_parse($fmt, '35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nОшибка: " . intl_get_error_message();
    echo "\nКод ошибки: " . intl_get_error_code();
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
    "dd/mm/yyyy"
);
echo "Снисходительность средства форматирования: ";
if ($fmt->isLenient()) {
    echo 'Да';
} else {
    echo 'Нет';
}
$fmt->parse('35/13/1971');
echo "\n Попытка выполнить синтаксический анализ '35/13/1971'.\nРезультат: " . $fmt->parse('35/13/1971');
if (intl_get_error_code() != 0){
    echo "\nОшибка: " . intl_get_error_message();
    echo "\nКод ошибки: " . intl_get_error_code();
}

$fmt->setLenient(FALSE);
echo 'Теперь снисходительность средства форматирования: ';
if ($fmt->isLenient()) {
    echo 'Да';
} else {
    echo 'Нет';
}
$fmt->parse('35/13/1971');
echo "\n Попытка выполнить синтаксический анализ '35/13/1971'.\nРезультат: " . $fmt->parse('35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nОшибка: " . intl_get_error_message();
    echo "\nКод ошибки: " . intl_get_error_code();
}

?>
```

Результат виконання цього прикладу:

```
Снисходительность средства форматирования: Да
Попытка выполнить синтаксический анализ '35/13/1971'.
Результат: -2147483
Теперь снисходительность средства форматирования: Нет
Попытка выполнить синтаксический анализ '35/13/1971'.
Результат:
Ошибка: Date parsing failed: U_PARSE_ERROR
Код ошибки: 9
```

### Дивіться також

-   [datefmtsetlenient()](intldateformatter.setlenient.html) - Встановлює м'який режим аналізатора
-   [datefmtcreate()](intldateformatter.create.html) - Створює засіб форматування дати
