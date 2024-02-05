---
navigation:
  - intlrulebasedbreakiterator.getrulestatusvec.md: '« IntlRuleBasedBreakIterator::getRuleStatusVec'
  - intlcodepointbreakiterator.getlastcodepoint.md: 'IntlCodePointBreakIterator::getLastCodePoint »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlCodePointBreakIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас IntlCodePointBreakIterator

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Цей [ітератор переривань](class.intlbreakiterator.md) вказує межі між кодами символів UTF-8.

## Огляд класів

```classsynopsis

    
     class IntlCodePointBreakIterator
    

    
     extends
      IntlBreakIterator
     {

    /* Наследуемые константы */
    
     public
     const
     int
      IntlBreakIterator::DONE;
public
     const
     int
      IntlBreakIterator::WORD_NONE;
public
     const
     int
      IntlBreakIterator::WORD_NONE_LIMIT;
public
     const
     int
      IntlBreakIterator::WORD_NUMBER;
public
     const
     int
      IntlBreakIterator::WORD_NUMBER_LIMIT;
public
     const
     int
      IntlBreakIterator::WORD_LETTER;
public
     const
     int
      IntlBreakIterator::WORD_LETTER_LIMIT;
public
     const
     int
      IntlBreakIterator::WORD_KANA;
public
     const
     int
      IntlBreakIterator::WORD_KANA_LIMIT;
public
     const
     int
      IntlBreakIterator::WORD_IDEO;
public
     const
     int
      IntlBreakIterator::WORD_IDEO_LIMIT;
public
     const
     int
      IntlBreakIterator::LINE_SOFT;
public
     const
     int
      IntlBreakIterator::LINE_SOFT_LIMIT;
public
     const
     int
      IntlBreakIterator::LINE_HARD;
public
     const
     int
      IntlBreakIterator::LINE_HARD_LIMIT;
public
     const
     int
      IntlBreakIterator::SENTENCE_TERM;
public
     const
     int
      IntlBreakIterator::SENTENCE_TERM_LIMIT;
public
     const
     int
      IntlBreakIterator::SENTENCE_SEP;
public
     const
     int
      IntlBreakIterator::SENTENCE_SEP_LIMIT;


    /* Методы */
    
   public getLastCodePoint(): int


    /* Наследуемые методы */
    public static IntlBreakIterator::createCharacterInstance(?string $locale = null): ?IntlBreakIterator
public static IntlBreakIterator::createCodePointInstance(): IntlCodePointBreakIterator
public static IntlBreakIterator::createLineInstance(?string $locale = null): ?IntlBreakIterator
public static IntlBreakIterator::createSentenceInstance(?string $locale = null): ?IntlBreakIterator
public static IntlBreakIterator::createTitleInstance(?string $locale = null): ?IntlBreakIterator
public static IntlBreakIterator::createWordInstance(?string $locale = null): ?IntlBreakIterator
public IntlBreakIterator::current(): int
public IntlBreakIterator::first(): int
public IntlBreakIterator::following(int $offset): int
public IntlBreakIterator::getErrorCode(): int
public IntlBreakIterator::getErrorMessage(): string
public IntlBreakIterator::getLocale(int $type): string|false
public IntlBreakIterator::getPartsIterator(string $type = IntlPartsIterator::KEY_SEQUENTIAL): IntlPartsIterator
public IntlBreakIterator::getText(): ?string
public IntlBreakIterator::isBoundary(int $offset): bool
public IntlBreakIterator::last(): int
public IntlBreakIterator::next(?int $offset = null): int
public IntlBreakIterator::preceding(int $offset): int
public IntlBreakIterator::previous(): int
public IntlBreakIterator::setText(string $text): bool

   }
```

## Зміст

-   [IntlCodePointBreakIterator::getLastCodePoint](intlcodepointbreakiterator.getlastcodepoint.md)— Отримати останній код символу, виданий під час переміщення ітератора вперед або назад
