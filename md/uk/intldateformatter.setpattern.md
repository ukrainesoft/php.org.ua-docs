Встановлює шаблон, який використовується IntlDateFormatter

-   [« IntlDateFormatter::setLenient](intldateformatter.setlenient.html)
    
-   [IntlDateFormatter::setTimeZone »](intldateformatter.settimezone.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Встановлює шаблон, який використовується IntlDateFormatter
    

# IntlDateFormatter::setPattern

# datefmtsetpattern

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::setPattern -- datefmtsetpattern — Встановлює шаблон, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::setPattern(string $pattern): bool
```

Процедурний стиль

```methodsynopsis
datefmt_set_pattern(IntlDateFormatter $formatter, string $pattern): bool
```

Встановлює шаблон, який використовується IntlDateFormatter.

### Список параметрів

`formatter`

Ресурс засобу форматування.

`pattern`

Новий рядок шаблон для використання. Можливі шаблони можна переглянути на [» https://unicode-org.github.io/icu/userguide/formatparse/datetime/](https://unicode-org.github.io/icu/userguide/format_parse/datetime/)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Зазвичай причиною помилки є погано відформатовані рядки.

### Приклади

**Приклад #1 Приклад використання **datefmtsetpattern()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'Шаблон средства форматирования : ', datefmt_get_pattern($fmt), PHP_EOL;
echo 'Первый отформатированный вывод : ', datefmt_format($fmt, 0), PHP_EOL;
datefmt_set_pattern($fmt, 'yyyyMMdd hh:mm:ss z');
echo 'Теперь шаблон средства форматирования : ', datefmt_get_pattern($fmt), PHP_EOL;
echo 'Второй отформатированный вывод : ', datefmt_format($fmt, 0), PHP_EOL;
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'Шаблон средства форматирования : ', $fmt->getPattern(), PHP_EOL;
echo 'Первый отформатированный вывод : ', $fmt->format(0), PHP_EOL;
$fmt->setPattern('yyyyMMdd hh:mm:ss z');
echo 'Теперь шаблон средства форматирования : ', $fmt->getPattern(), PHP_EOL;
echo 'Второй отформатированный вывод : ', $fmt->format(0), PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
Шаблон средства форматирования : MM/dd/yyyy
Первый отформатированный вывод : 12/31/1969
Теперь шаблон средства форматирования : yyyyMMdd hh:mm:ss z
Второй отформатированный вывод : 19691231 04:00:00 PST
```

### Дивіться також

-   [datefmtgetpattern()](intldateformatter.getpattern.html) - Отримує шаблон, який використовується IntlDateFormatter
-   [datefmtcreate()](intldateformatter.create.html) - Створює засіб форматування дати