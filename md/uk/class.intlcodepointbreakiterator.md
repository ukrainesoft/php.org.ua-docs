Клас IntlCodePointBreakIterator

-   [« IntlRuleBasedBreakIterator::getRuleStatusVec](intlrulebasedbreakiterator.getrulestatusvec.md)
    
-   [IntlCodePointBreakIterator::getLastCodePoint »](intlcodepointbreakiterator.getlastcodepoint.md)
    
-   [PHP Manual](index.md)
    
-   [intl](book.intl.md)
    
-   Клас IntlCodePointBreakIterator
    

# Клас IntlCodePointBreakIterator

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Цей [ітератор переривань](class.intlbreakiterator.md) вказує межі між кодами символів UTF-8.

## Огляд класів

```classsynopsis

     
    

    
     
      class IntlCodePointBreakIterator
     

     
      extends
       IntlBreakIterator
     
     {

    /* Наследуемые константы */
    
     const
     int
      IntlBreakIterator::DONE = -1;
const
     int
      IntlBreakIterator::WORD_NONE = 0;
const
     int
      IntlBreakIterator::WORD_NONE_LIMIT = 100;
const
     int
      IntlBreakIterator::WORD_NUMBER = 100;
const
     int
      IntlBreakIterator::WORD_NUMBER_LIMIT = 200;
const
     int
      IntlBreakIterator::WORD_LETTER = 200;
const
     int
      IntlBreakIterator::WORD_LETTER_LIMIT = 300;
const
     int
      IntlBreakIterator::WORD_KANA = 300;
const
     int
      IntlBreakIterator::WORD_KANA_LIMIT = 400;
const
     int
      IntlBreakIterator::WORD_IDEO = 400;
const
     int
      IntlBreakIterator::WORD_IDEO_LIMIT = 500;
const
     int
      IntlBreakIterator::LINE_SOFT = 0;
const
     int
      IntlBreakIterator::LINE_SOFT_LIMIT = 100;
const
     int
      IntlBreakIterator::LINE_HARD = 100;
const
     int
      IntlBreakIterator::LINE_HARD_LIMIT = 200;
const
     int
      IntlBreakIterator::SENTENCE_TERM = 0;
const
     int
      IntlBreakIterator::SENTENCE_TERM_LIMIT = 100;
const
     int
      IntlBreakIterator::SENTENCE_SEP = 100;
const
     int
      IntlBreakIterator::SENTENCE_SEP_LIMIT = 200;


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
intl_get_error_code(): int
public IntlBreakIterator::getErrorMessage(): string|false
intl_get_error_message(): string
public IntlBreakIterator::getLocale(int $type): string
public IntlBreakIterator::getPartsIterator(string $type = IntlPartsIterator::KEY_SEQUENTIAL): IntlPartsIterator
public IntlBreakIterator::getText(): ?string
public IntlBreakIterator::isBoundary(int $offset): bool
public IntlBreakIterator::last(): int
public IntlBreakIterator::next(?int $offset = null): int
public IntlBreakIterator::preceding(int $offset): int
public IntlBreakIterator::previous(): int
public IntlBreakIterator::setText(string $text): ?bool

   }
```

## Зміст

-   [IntlCodePointBreakIterator::getLastCodePoint](intlcodepointbreakiterator.getlastcodepoint.md) — Отримати останній код символу, виданий під час переміщення ітератора вперед чи назад