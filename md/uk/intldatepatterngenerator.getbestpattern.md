- [« IntlDatePatternGenerator::create](intldatepatterngenerator.create.md)
- [IntlPartsIterator »](class.intlpartsiterator.md)

- [PHP Manual](index.md)
- [IntlDatePatternGenerator](class.intldatepatterngenerator.md)
- Визначає найбільш підходящий формат дати/часу

# IntlDatePatternGenerator::getBestPattern

(PHP 8 \>= 8.1.0)

IntlDatePatternGenerator::getBestPattern — Визначає найбільш
відповідний формат дати/часу

### Опис

public **IntlDatePatternGenerator::getBestPattern**(string `$skeleton`):
string\|false

Визначає, який формат дати/часу найбільше підходить для конкретної
локалі.

### Список параметрів

`skeleton`
Каркас.

### Значення, що повертаються

Повертає формат, який приймається
[DateTimeInterface::format()](datetime.format.md) у разі успішного
виконання, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання
**IntlDatePatternGenerator::getBestPattern()****

` <?php$skeleton = 'YYYYMMdd';$today = \DateTimeImmutable::createFromFormat('Y-m-d', '2021-04-24');$patternGenerator = new \IntlDatePat $patternGenerator->getBestPattern($skeleton);echo 'Німецька: ', \IntlDateFormatter::formatObject($today, $pattern, 'de_DE'), "
";$patternGenerator = new \IntlDatePatternGenerator('en_US');$pattern = $patternGenerator->getBestPattern($skeleton);echo 'Англійська: ', \IntlDateFormatter::formatObject'$ ?> `

Результат виконання цього прикладу:

Німецька: 24.04.2021
Англійська: 04/24/2021
