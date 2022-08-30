Створює новий екземпляр IntlDatePatternGenerator

-   [« IntlDatePatternGenerator](class.intldatepatterngenerator.html)
    
-   [IntlDatePatternGenerator::getBestPattern »](intldatepatterngenerator.getbestpattern.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDatePatternGenerator](class.intldatepatterngenerator.html)
    
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

Створює новий екземпляр [IntlDatePatternGenerator](class.intldatepatterngenerator.html)

### Список параметрів

`locale`

Локаль. Якщо передано значення **`null`**, використовується ini-параметр [intl.defaultlocale](intl.configuration.html#ini.intl.default-locale)

### Значення, що повертаються

Повертає екземпляр [IntlDatePatternGenerator](class.intldatepatterngenerator.html) у разі успішного виконання або **`null`** у разі виникнення помилки.