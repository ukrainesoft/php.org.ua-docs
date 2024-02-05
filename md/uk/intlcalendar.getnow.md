---
navigation:
  - intlcalendar.getminimum.md: '« IntlCalendar::getMinimum'
  - intlcalendar.getrepeatedwalltimeoption.md: 'IntlCalendar::getRepeatedWallTimeOption »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getNow'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getNow

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getNow — Отримує число, яке представляє поточний час

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlCalendar::getNow(): float
```

Процедурний стиль

```methodsynopsis
intlcal_get_now(): float
```

Кількість мілісекунд, що минули від початку епохи Unix. Число визначається системним часом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Число з плаваючою точкою (float), що представляє кількість мілісекунд з початку епохи Unix, крім додаткових секунд.

### Приклади

**Пример #1 Пример использования**IntlCalendar::getNow()\*\*\*\*

```php
<?php
$formatter = IntlDateFormatter::create('es_ES',
        IntlDateFormatter::FULL,
        IntlDateFormatter::FULL,
        'Europe/Madrid');

$val = IntlCalendar::getNow();

var_dump($val);
echo $formatter->format(IntlCalendar::getNow() / 1000.), "\n";
```

Результат виконання наведеного прикладу:

```
float(1371425814666)
lunes, 17 de junio de 2013 01:36:54 Hora de verano de Europa central
```
