---
navigation:
  - function.nl2br.md: « nl2br
  - function.ord.md: ord »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: number\_format
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# number\_format

(PHP 4, PHP 5, PHP 7, PHP 8)

number\_format — Форматує число з розділенням груп

### Опис

```methodsynopsis
number_format(    float $num,    int $decimals = 0,    ?string $decimal_separator = ".",    ?string $thousands_separator = ","): string
```

Форматує число згрупованими тисячними та, можливо, десятковими цифрами, використовуючи математичне правило округлення.

### Список параметрів

`num`

Форматоване число.

`decimals`

Встановлює кількість знаків після коми. Якщо `decimal_separator` опускається у значенні, що повертається.

`decimal_separator`

Встановлює роздільник дробової частини.

`thousands_separator`

Встановлює роздільник тисяч.

### Значення, що повертаються

Відформатована кількість `num`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | До цієї версії функція **number\_format()** приймала один, два чи чотири параметри (але не три). |
| 7.2.0 | **number\_format()** була змінена, щоб не повертати `-0`, раніше `-0` могло бути повернено у випадках, коли `num` був `-0.01` |

### Приклади

**Пример #1 Пример использования**number\_format()\*\*\*\*

У Франції зазвичай використовуються 2 знаки після коми (','), і пробіл ('') як роздільник груп. Цей приклад демонструє різні способи форматування чисел:

```php
<?php

$number = 1234.56;

// английский формат (по умолчанию)
$english_format_number = number_format($number);
// 1,235

// французский формат
$nombre_format_francais = number_format($number, 2, ',', ' ');
// 1 234,56

$number = 1234.5678;

// английский формат без разделителей групп
$english_format_number = number_format($number, 2, '.', '');
// 1234.57

?>
```

### Дивіться також

-   [money\_format()](function.money-format.md) \- Форматує число як грошову величину
-   [sprintf()](function.sprintf.md) \- Повертає відформатований рядок
-   [printf()](function.printf.md) \- Виводить відформатований рядок
-   [sscanf()](function.sscanf.md) \- Розбирає рядок відповідно до заданого формату
