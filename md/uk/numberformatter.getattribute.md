- [«NumberFormatter::format](numberformatter.format.md)
- [NumberFormatter::getErrorCode »](numberformatter.geterrorcode.md)

- [PHP Manual](index.md)
- [NumberFormatter](class.numberformatter.md)
- Отримує атрибут

# NumberFormatter::getAttribute

#numfmt_get_attribute

(PHP 5 = 5.3.0, PHP 7, PHP 8, PECL intl = 1.0.0)

NumberFormatter::getAttribute -- numfmt_get_attribute -- Отримує атрибут

### Опис

Об'єктно-орієнтований стиль

public **NumberFormatter::getAttribute**(int `$attribute`):
int\|float\|false

Процедурний стиль

**numfmt_get_attribute**([NumberFormatter](class.numberformatter.md)
`$formatter`, int `$attribute`): int\|float\|false

Отримує числовий атрибут, пов'язаний із засобом форматування.
Прикладом числового атрибуту є кількість цілих цифр, яка
видаватиме засіб форматування.

### Список параметрів

`formatter`
Об'єкт [NumberFormatter](class.numberformatter.md).

`attribute`
Специфікатор атрибута - одна з констант [числового атрибута](class.numberformatter.md#intl.numberformatter-constants.unumberformatattribute).

### Значення, що повертаються

Повертає значення атрибута у разі успішного виконання або
**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **numfmt_get_attribute()****

` <?php$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );echo "Цифр: ".numfmt_get_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGI
";echo numfmt_format($fmt, 1234567.891234567890000)."
";numfmt_set_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS, 2);echo "Цифр: ".numfmt_get_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS)."
";echo numfmt_format($fmt, 1234567.891234567890000)."
";?> `

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

` <?php$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );echo "Digits: ".$fmt->getAttribute(NumberFormatter::MAX_FRACTION_DIGITS)."
";echo $fmt->format(1234567.891234567890000)."
";$fmt->setAttribute(NumberFormatter::MAX_FRACTION_DIGITS, 2);echo "Digits: ".$fmt->getAttribute(NumberFormatter::MAX_FRACTION_DIGITS)."
";echo $fmt->format(1234567.891234567890000)."
";?> `

Результат виконання цього прикладу:

Цифр: 3
1.234.567,891
Цифр: 2
1.234.567,89

### Дивіться також

- [numfmt_get_error_code()](numberformatter.geterrorcode.md) -
Отримує останній код помилки засобу форматування
- [numfmt_get_text_attribute()](numberformatter.gettextattribute.md) -
Отримує текстовий атрибут
- [numfmt_set_attribute()](numberformatter.setattribute.md) -
Встановлює атрибут
