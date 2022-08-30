Створює новий екземпляр IntlDatePatternGenerator

-   [« IntlDatePatternGenerator](class.intldatepatterngenerator.md)
    
-   [IntlDatePatternGenerator::getBestPattern »](intldatepatterngenerator.getbestpattern.md)
    
-   [PHP Manual](index.md)
    
-   [IntlDatePatternGenerator](class.intldatepatterngenerator.md)
    
-   Створює новий екземпляр IntlDatePatternGenerator
    

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