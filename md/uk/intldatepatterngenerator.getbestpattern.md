---
navigation:
  - intldatepatterngenerator.create.md: '« IntlDatePatternGenerator::create'
  - class.intlpartsiterator.md: IntlPartsIterator »
  - index.md: PHP Manual
  - class.intldatepatterngenerator.md: IntlDatePatternGenerator
title: 'IntlDatePatternGenerator::getBestPattern'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDatePatternGenerator::getBestPattern

(PHP 8 >= 8.1.0)

IntlDatePatternGenerator::getBestPattern — Визначає найбільш вдалий формат дати/часу

### Опис

```methodsynopsis
public IntlDatePatternGenerator::getBestPattern(string $skeleton): string|false
```

Визначає, який формат дати/часу найбільше підходить для конкретної локалі.

### Список параметрів

`skeleton`

Каркас.

### Значення, що повертаються

Повертає формат, який приймається [DateTimeInterface::format()](datetime.format.md) у разі успішного виконання, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**IntlDatePatternGenerator::getBestPattern()\*\*\*\*

```php
<?php

$skeleton = 'YYYYMMdd';
$today = \DateTimeImmutable::createFromFormat('Y-m-d', '2021-04-24');

$patternGenerator = new \IntlDatePatternGenerator('de_DE');
$pattern = $patternGenerator->getBestPattern($skeleton);
echo 'Немецкий: ', \IntlDateFormatter::formatObject($today, $pattern, 'de_DE'), "\n";

$patternGenerator = new \IntlDatePatternGenerator('en_US');
$pattern = $patternGenerator->getBestPattern($skeleton);
echo 'Английский: ', \IntlDateFormatter::formatObject($today, $pattern, 'en_US');
?>
```

Результат виконання наведеного прикладу:

```
Немецкий: 24.04.2021
Английский: 04/24/2021
```
