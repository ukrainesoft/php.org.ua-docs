Клас IntlDatePatternGenerator

-   [« IntlCodePointBreakIterator::getLastCodePoint](intlcodepointbreakiterator.getlastcodepoint.html)
    
-   [IntlDatePatternGenerator::create »](intldatepatterngenerator.create.html)
    
-   [PHP Manual](index.html)
    
-   [intl](book.intl.html)
    
-   Клас IntlDatePatternGenerator
    

# Клас IntlDatePatternGenerator

(PHP 8> = 8.1.0)

## Вступ

Створює локалізовані рядки шаблонів формату дати та/або часу, які підходять для використання в [IntlDateFormatter](class.intldateformatter.html)

## Огляд класів

```classsynopsis

     
    

    
     
      class IntlDatePatternGenerator
     
     {

    /* Методы */
    
   public __construct(string $locale = null)

    public static create(string $locale = null): ?IntlDatePatternGenerator
public getBestPattern(string $skeleton): string|false

   }
```

## Зміст

-   [IntlDatePatternGenerator::create](intldatepatterngenerator.create.html) — Створює новий екземпляр IntlDatePatternGenerator
-   [IntlDatePatternGenerator::getBestPattern](intldatepatterngenerator.getbestpattern.html) — Визначає найбільш підходящий формат дати/часу