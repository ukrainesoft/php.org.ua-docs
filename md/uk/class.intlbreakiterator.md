Клас IntlBreakIterator

-   [« Transliterator::transliterate](transliterator.transliterate.html)
    
-   [IntlBreakIterator::\_\_construct »](intlbreakiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [intl](book.intl.html)
    
-   Клас IntlBreakIterator
    

# Клас IntlBreakIterator

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Ітератор переривання (Break iterator) - це об'єкт ICU, що надає методи для визначення меж у тексті (наприклад межі слова або речення). У PHP клас **IntlBreakIterator** служить базовим класом всім типів ітераторів переривання ICU. Є й додаткова функціональність, модуль intl може розширювати цей клас відповідними підкласами, такими як [IntlRuleBasedBreakIterator](class.intlrulebasedbreakiterator.html) або [IntlCodePointBreakIterator](class.intlcodepointbreakiterator.html)

Цей клас реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html). Traversing an Ітерація **IntlBreakIterator** породжує невід'ємні цілі значення, що являють собою успішне знаходження кордонів у тексті, і рівні позиції знайденого символу UTF-8 відрахованої від початку тексту (позиція першого символу дорівнює `0`). Ключі повернутих значень являють собою послідовність натуральних чисел `{0, 1, 2, …}`

## Огляд класів

```classsynopsis

     
    

    
     
      class IntlBreakIterator
     

     implements 
       IteratorAggregate {

    /* Константы */
    
     const
     int
      DONE = -1;

    const
     int
      WORD_NONE = 0;

    const
     int
      WORD_NONE_LIMIT = 100;

    const
     int
      WORD_NUMBER = 100;

    const
     int
      WORD_NUMBER_LIMIT = 200;

    const
     int
      WORD_LETTER = 200;

    const
     int
      WORD_LETTER_LIMIT = 300;

    const
     int
      WORD_KANA = 300;

    const
     int
      WORD_KANA_LIMIT = 400;

    const
     int
      WORD_IDEO = 400;

    const
     int
      WORD_IDEO_LIMIT = 500;

    const
     int
      LINE_SOFT = 0;

    const
     int
      LINE_SOFT_LIMIT = 100;

    const
     int
      LINE_HARD = 100;

    const
     int
      LINE_HARD_LIMIT = 200;

    const
     int
      SENTENCE_TERM = 0;

    const
     int
      SENTENCE_TERM_LIMIT = 100;

    const
     int
      SENTENCE_SEP = 100;

    const
     int
      SENTENCE_SEP_LIMIT = 200;


    /* Методы */
    
   private __construct()

    public static createCharacterInstance(?string $locale = null): ?IntlBreakIterator
public static createCodePointInstance(): IntlCodePointBreakIterator
public static createLineInstance(?string $locale = null): ?IntlBreakIterator
public static createSentenceInstance(?string $locale = null): ?IntlBreakIterator
public static createTitleInstance(?string $locale = null): ?IntlBreakIterator
public static createWordInstance(?string $locale = null): ?IntlBreakIterator
public current(): int
public first(): int
public following(int $offset): int
public getErrorCode(): int
intl_get_error_code(): int
public getErrorMessage(): string|false
intl_get_error_message(): string
public getLocale(int $type): string
public getPartsIterator(string $type = IntlPartsIterator::KEY_SEQUENTIAL): IntlPartsIterator
public getText(): ?string
public isBoundary(int $offset): bool
public last(): int
public next(?int $offset = null): int
public preceding(int $offset): int
public previous(): int
public setText(string $text): ?bool

   }
```

## Обумовлені константи

**`IntlBreakIterator::DONE`**

**`IntlBreakIterator::WORD_NONE`**

**`IntlBreakIterator::WORD_NONE_LIMIT`**

**`IntlBreakIterator::WORD_NUMBER`**

**`IntlBreakIterator::WORD_NUMBER_LIMIT`**

**`IntlBreakIterator::WORD_LETTER`**

**`IntlBreakIterator::WORD_LETTER_LIMIT`**

**`IntlBreakIterator::WORD_KANA`**

**`IntlBreakIterator::WORD_KANA_LIMIT`**

**`IntlBreakIterator::WORD_IDEO`**

**`IntlBreakIterator::WORD_IDEO_LIMIT`**

**`IntlBreakIterator::LINE_SOFT`**

**`IntlBreakIterator::LINE_SOFT_LIMIT`**

**`IntlBreakIterator::LINE_HARD`**

**`IntlBreakIterator::LINE_HARD_LIMIT`**

**`IntlBreakIterator::SENTENCE_TERM`**

**`IntlBreakIterator::SENTENCE_TERM_LIMIT`**

**`IntlBreakIterator::SENTENCE_SEP`**

**`IntlBreakIterator::SENTENCE_SEP_LIMIT`**

## список змін

| Версия | Описание                                                                                                                                                                                 |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Клас **IntlBreakIterator** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html). Раніше натомість було реалізовано інтерфейс [Traversable](class.traversable.html) |

## Зміст

-   [IntlBreakIterator::\_\_construct](intlbreakiterator.construct.html) — Закритий конструктор, який забороняє створення екземплярів об'єкту
-   [IntlBreakIterator::createCharacterInstance](intlbreakiterator.createcharacterinstance.html) — Створює ітератор переривання меж комбінування послідовностей символів.
-   [IntlBreakIterator::createCodePointInstance](intlbreakiterator.createcodepointinstance.html) — Створює ітератор переривання меж кодових точок.
-   [IntlBreakIterator::createLineInstance](intlbreakiterator.createlineinstance.html) — Створює ітератор переривання для логічно можливих розривів рядків
-   [IntlBreakIterator::createSentenceInstance](intlbreakiterator.createsentenceinstance.html) - Створює ітератор переривання для розривів речень
-   [IntlBreakIterator::createTitleInstance](intlbreakiterator.createtitleinstance.html) - Створює ітератор переривання для розривів заголовків
-   [IntlBreakIterator::createWordInstance](intlbreakiterator.createwordinstance.html) - Створює ітератор переривання для розривів слів
-   [IntlBreakIterator::current](intlbreakiterator.current.html) — Повертає індекс поточної позиції
-   [IntlBreakIterator::first](intlbreakiterator.first.html) — Встановлює позицію першого символу в тексті
-   [IntlBreakIterator::following](intlbreakiterator.following.html) — Переміщає ітератор до першого кордону після вказаного усунення
-   [IntlBreakIterator::getErrorCode](intlbreakiterator.geterrorcode.html) — Повертає останній код помилки об'єкту
-   [IntlBreakIterator::getErrorMessage](intlbreakiterator.geterrormessage.html) — Повертає останнє повідомлення про помилку об'єкта
-   [IntlBreakIterator::getLocale](intlbreakiterator.getlocale.html) — Повертає локаль, пов'язану з об'єктом
-   [IntlBreakIterator::getPartsIterator](intlbreakiterator.getpartsiterator.html) — створює ітератор для переміщення фрагментів між кордонами.
-   [IntlBreakIterator::getText](intlbreakiterator.gettext.html) — Повертає текст, що сканується.
-   [IntlBreakIterator::isBoundary](intlbreakiterator.isboundary.html) — Повідомляє, чи є усунення зміщенням кордону
-   [IntlBreakIterator::last](intlbreakiterator.last.html) — Встановлює позицію ітератора до індексу за останнім символом
-   [IntlBreakIterator::next](intlbreakiterator.next.html) — Переміщує ітератор до наступного кордону
-   [IntlBreakIterator::preceding](intlbreakiterator.preceding.html) — Встановлює позицію ітератора до першого кордону перед усуненням
-   [IntlBreakIterator::previous](intlbreakiterator.previous.html) — Встановлює позицію ітератора на кордоні безпосередньо перед поточною
-   [IntlBreakIterator::setText](intlbreakiterator.settext.html) — Встановлює сканований текст