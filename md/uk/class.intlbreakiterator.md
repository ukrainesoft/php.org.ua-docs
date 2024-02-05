---
navigation:
  - transliterator.transliterate.md: '« Transliterator::transliterate'
  - intlbreakiterator.construct.md: 'IntlBreakIterator::\_\_construct »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlBreakIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас IntlBreakIterator

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Ітератор переривання (Break iterator) - це об'єкт ICU, що надає методи для визначення меж у тексті (наприклад межі слова або речення). У PHP клас **IntlBreakIterator** служить базовим класом всім типів ітераторів переривання ICU. Є й додаткова функціональність, модуль intl може розширювати цей клас відповідними підкласами, такими як [IntlRuleBasedBreakIterator](class.intlrulebasedbreakiterator.md) або [IntlCodePointBreakIterator](class.intlcodepointbreakiterator.md)

Цей клас реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md)Traversing an Итерация**IntlBreakIterator** породжує невід'ємні цілі значення, що являють собою успішне знаходження кордонів у тексті, і рівні позиції знайденого символу UTF-8 відрахованої від початку тексту (позиція першого символу дорівнює ). Ключі повернутих значень являють собою послідовність натуральних чисел `{0, 1, 2, …}`

## Огляд класів

```classsynopsis

    
     class IntlBreakIterator
    

    
     implements
      IteratorAggregate {

    /* Константы */
    
     public
     const
     int
      DONE;

    public
     const
     int
      WORD_NONE;

    public
     const
     int
      WORD_NONE_LIMIT;

    public
     const
     int
      WORD_NUMBER;

    public
     const
     int
      WORD_NUMBER_LIMIT;

    public
     const
     int
      WORD_LETTER;

    public
     const
     int
      WORD_LETTER_LIMIT;

    public
     const
     int
      WORD_KANA;

    public
     const
     int
      WORD_KANA_LIMIT;

    public
     const
     int
      WORD_IDEO;

    public
     const
     int
      WORD_IDEO_LIMIT;

    public
     const
     int
      LINE_SOFT;

    public
     const
     int
      LINE_SOFT_LIMIT;

    public
     const
     int
      LINE_HARD;

    public
     const
     int
      LINE_HARD_LIMIT;

    public
     const
     int
      SENTENCE_TERM;

    public
     const
     int
      SENTENCE_TERM_LIMIT;

    public
     const
     int
      SENTENCE_SEP;

    public
     const
     int
      SENTENCE_SEP_LIMIT;


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
public getErrorMessage(): string
public getLocale(int $type): string|false
public getPartsIterator(string $type = IntlPartsIterator::KEY_SEQUENTIAL): IntlPartsIterator
public getText(): ?string
public isBoundary(int $offset): bool
public last(): int
public next(?int $offset = null): int
public preceding(int $offset): int
public previous(): int
public setText(string $text): bool

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

| Версия | Опис |
| --- | --- |
| 8.0.0 | Класс**IntlBreakIterator** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md). . Раніше натомість було реалізовано інтерфейс [Traversable](class.traversable.md) |

## Зміст

-   [IntlBreakIterator::\_\_construct](intlbreakiterator.construct.md)— Закритий конструктор, який забороняє створення екземплярів об'єкту
-   [IntlBreakIterator::createCharacterInstance](intlbreakiterator.createcharacterinstance.md)— Створює ітератор переривання меж комбінування послідовностей символів.
-   [IntlBreakIterator::createCodePointInstance](intlbreakiterator.createcodepointinstance.md)— Створює ітератор переривання меж кодових точок.
-   [IntlBreakIterator::createLineInstance](intlbreakiterator.createlineinstance.md)— Створює ітератор переривання для логічно можливих розривів рядків
-   [IntlBreakIterator::createSentenceInstance](intlbreakiterator.createsentenceinstance.md) \- Створює ітератор переривання для розривів речень
-   [IntlBreakIterator::createTitleInstance](intlbreakiterator.createtitleinstance.md) \- Створює ітератор переривання для розривів заголовків
-   [IntlBreakIterator::createWordInstance](intlbreakiterator.createwordinstance.md) \- Створює ітератор переривання для розривів слів
-   [IntlBreakIterator::current](intlbreakiterator.current.md)— Повертає індекс поточної позиції
-   [IntlBreakIterator::first](intlbreakiterator.first.md)— Встановлює позицію першого символу в тексті
-   [IntlBreakIterator::following](intlbreakiterator.following.md)— Переміщає ітератор до першого кордону після вказаного усунення
-   [IntlBreakIterator::getErrorCode](intlbreakiterator.geterrorcode.md)— Повертає останній код помилки об'єкту
-   [IntlBreakIterator::getErrorMessage](intlbreakiterator.geterrormessage.md)— Повертає останнє повідомлення про помилку об'єкта
-   [IntlBreakIterator::getLocale](intlbreakiterator.getlocale.md)— Повертає локаль, пов'язану з об'єктом
-   [IntlBreakIterator::getPartsIterator](intlbreakiterator.getpartsiterator.md)— створює ітератор для переміщення фрагментів між кордонами.
-   [IntlBreakIterator::getText](intlbreakiterator.gettext.md)— Повертає текст, що сканується.
-   [IntlBreakIterator::isBoundary](intlbreakiterator.isboundary.md)— Повідомляє, чи є усунення зміщенням кордону
-   [IntlBreakIterator::last](intlbreakiterator.last.md)— Встановлює позицію ітератора до індексу за останнім символом
-   [IntlBreakIterator::next](intlbreakiterator.next.md)— Переміщує ітератор до наступного кордону
-   [IntlBreakIterator::preceding](intlbreakiterator.preceding.md)— Встановлює позицію ітератора до першого кордону перед усуненням
-   [IntlBreakIterator::previous](intlbreakiterator.previous.md)— Встановлює позицію ітератора на кордоні безпосередньо перед поточною
-   [IntlBreakIterator::setText](intlbreakiterator.settext.md)— Встановлює сканований текст
