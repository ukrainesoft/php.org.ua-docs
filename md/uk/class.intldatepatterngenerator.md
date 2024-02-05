---
navigation:
  - intlcodepointbreakiterator.getlastcodepoint.md: '« IntlCodePointBreakIterator::getLastCodePoint'
  - intldatepatterngenerator.create.md: 'IntlDatePatternGenerator::create »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlDatePatternGenerator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас IntlDatePatternGenerator

(PHP 8 >= 8.1.0)

## Вступ

Створює локалізовані рядки шаблонів формату дати та/або часу, які підходять для використання в [IntlDateFormatter](class.intldateformatter.md)

## Огляд класів

```classsynopsis

    
     class IntlDatePatternGenerator
     {

    /* Методы */
    
   public __construct(?string $locale = null)

    public static create(?string $locale = null): ?IntlDatePatternGenerator
public getBestPattern(string $skeleton): string|false

   }
```

## Зміст

-   [IntlDatePatternGenerator::create](intldatepatterngenerator.create.md)— Створює новий екземпляр IntlDatePatternGenerator
-   [IntlDatePatternGenerator::getBestPattern](intldatepatterngenerator.getbestpattern.md)— Визначає найбільш підходящий формат дати/часу
