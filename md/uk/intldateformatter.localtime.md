Перетворює рядок на значення часу на основі поля

-   [« IntlDateFormatter::isLenient](intldateformatter.islenient.html)
    
-   [IntlDateFormatter::parse »](intldateformatter.parse.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Перетворює рядок на значення часу на основі поля
    

# IntlDateFormatter::localtime

# datefmtlocaltime

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::localtime -- datefmtlocaltime — Перетворення строку на значення часу на основі поля

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::localtime(string $string, int &$offset = null): array|false
```

Процедурний стиль

```methodsynopsis
datefmt_localtime(IntlDateFormatter $formatter, string $string, int &$offset = null): array|false
```

Перетворює рядок $value на значення часу на основі полів (масив різних полів), починаючи з $parsepos і використовуючи якомога більшу частину вхідного значення.

### Список параметрів

`formatter`

Ресурс засобу форматування.

`string`

Рядок для перетворення під час.

`offset`

Позиція, з якої слід розпочати синтаксичний аналіз $value (починаючи з нуля). Якщо до використання $value помилки не виникає, $parsepos міститиме -1, інакше він міститиме позицію, у якій закінчився синтаксичний аналіз. Якщо $parsepos > `strlen($value)`, аналіз негайно завершується помилкою.

### Значення, що повертаються

Масив цілих чисел, сумісний із місцевим часом: містить 24-годинне значення у полі tmhour або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtlocaltime()****

```php
<?php

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$arr = datefmt_localtime($fmt, 'Wednesday, December 31, 1969 4:00:00 PM PT', 0);
echo 'Преобразованный вывод: ';
if ($arr) {
    foreach ($arr as $key => $value) {
        echo "$key : $value , ";
    }
}

?>
```

**Приклад #2 OO example**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$arr = $fmt->localtime('Wednesday, December 31, 1969 4:00:00 PM PT', 0);
echo 'Преобразованный вывод: ';
if ($arr) {
    foreach ($arr as $key => $value) {
        echo "$key : $value , ";
    }
}

?>
```

Результат виконання цього прикладу:

```
Преобразованный вывод: tm_sec : 0 , tm_min : 0 , tm_hour : 16 , tm_year : 1969 ,
tm_mday : 31 , tm_wday : 4 , tm_yday : 365 , tm_mon : 11 , tm_isdst : 0 ,
```

### Дивіться також

-   [datefmt\_create()](intldateformatter.create.html) - Створює засіб форматування дати
-   [datefmt\_format()](intldateformatter.format.html) - Форматує значення дати/часу у вигляді рядка
-   [datefmt\_parse()](intldateformatter.parse.html) - Перетворює рядок на значення позначки часу
-   [datefmt\_get\_error\_code()](intldateformatter.geterrorcode.html) - Отримує код помилки останньої операції
-   [datefmt\_get\_error\_message()](intldateformatter.geterrormessage.html) - Отримує текст помилки останньої операції