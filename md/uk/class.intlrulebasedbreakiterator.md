---
navigation:
  - intlbreakiterator.settext.md: '« IntlBreakIterator::setText'
  - intlrulebasedbreakiterator.construct.md: 'IntlRuleBasedBreakIterator::\_\_construct »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlRuleBasedBreakIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас IntlRuleBasedBreakIterator

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Подкласс[IntlBreakIterator](class.intlbreakiterator.md), який реалізує ітератор переривань ICU, чия поведінка задано набором правил. Це найчастіше використовуваний тип ітератора переривань.

Правила описані у розділі [» Посібник користувача з аналізу кордонів ICU](https://unicode-org.github.io/icu/userguide/boundaryanalysis/break-rules.md)

## Огляд класів

```classsynopsis

    
     class IntlRuleBasedBreakIterator
    

    
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
    
   public __construct(string $rules, bool $compiled = false)

    public getBinaryRules(): string|false
public getRules(): string|false
public getRuleStatus(): int
public getRuleStatusVec(): array|false


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

-   [IntlRuleBasedBreakIterator::\_\_construct](intlrulebasedbreakiterator.construct.md) \- Створює ітератор на основі набору правил
-   [IntlRuleBasedBreakIterator::getBinaryRules](intlrulebasedbreakiterator.getbinaryrules.md)— Отримати бінарні дані зі скомпілованих правил
-   [IntlRuleBasedBreakIterator::getRules](intlrulebasedbreakiterator.getrules.md)— Отримати набір правил, які використовуються під час створення цього об'єкта
-   [IntlRuleBasedBreakIterator::getRuleStatus](intlrulebasedbreakiterator.getrulestatus.md)— Отримати найбільше значення статусу правил зупинки, що визначило поточну позицію зупинки
-   [IntlRuleBasedBreakIterator::getRuleStatusVec](intlrulebasedbreakiterator.getrulestatusvec.md)— отримати значення статусів із правил зупинки, які визначили поточну позицію зупинки
