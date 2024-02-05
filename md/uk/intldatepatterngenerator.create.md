---
navigation:
  - class.intldatepatterngenerator.md: « IntlDatePatternGenerator
  - intldatepatterngenerator.getbestpattern.md: 'IntlDatePatternGenerator::getBestPattern »'
  - index.md: PHP Manual
  - class.intldatepatterngenerator.md: IntlDatePatternGenerator
title: 'IntlDatePatternGenerator::create'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDatePatternGenerator::create

# IntlDatePatternGenerator::\_\_construct

(PHP 8 >= 8.1.0)

IntlDatePatternGenerator::create -- IntlDatePatternGenerator::\_\_construct — Створює новий екземпляр IntlDatePatternGenerator

### Опис

```methodsynopsis
public static IntlDatePatternGenerator::create(?string $locale = null): ?IntlDatePatternGenerator
```

public**IntlDatePatternGenerator::\_\_construct**(?string`$locale` **`null`**) .

Створює новий екземпляр [IntlDatePatternGenerator](class.intldatepatterngenerator.md)

### Список параметрів

`locale`

Локаль. Якщо передано значення **`null`**, используется ini-параметр[intl.default\_locale](intl.configuration.md#ini.intl.default-locale)

### Значення, що повертаються

Повертає екземпляр [IntlDatePatternGenerator](class.intldatepatterngenerator.md) у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.
