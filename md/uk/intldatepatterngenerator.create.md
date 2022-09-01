---
navigation:
  - class.intldatepatterngenerator.md: « IntlDatePatternGenerator
  - intldatepatterngenerator.getbestpattern.md: 'IntlDatePatternGenerator::getBestPattern »'
  - index.md: PHP Manual
  - class.intldatepatterngenerator.md: IntlDatePatternGenerator
title: 'IntlDatePatternGenerator::create'
---
# IntlDatePatternGenerator::create

# IntlDatePatternGenerator::construct

(PHP 8> = 8.1.0)

Intl Date Pattern Generator::create -- Intl Date Pattern Generator::construct — Створює новий екземпляр IntlDatePatternGenerator

### Опис

```methodsynopsis
public static IntlDatePatternGenerator::create(string $locale = null): ?IntlDatePatternGenerator
```

public **IntlDatePatternGenerator::construct**(string `$locale` **`null`**

Створює новий екземпляр [IntlDatePatternGenerator](class.intldatepatterngenerator.md)

### Список параметрів

`locale`

Локаль. Якщо передано значення **`null`**, використовується ini-параметр [intl.defaultlocale](intl.configuration.html#ini.intl.default-locale)

### Значення, що повертаються

Повертає екземпляр [IntlDatePatternGenerator](class.intldatepatterngenerator.md) у разі успішного виконання або **`null`** у разі виникнення помилки.
