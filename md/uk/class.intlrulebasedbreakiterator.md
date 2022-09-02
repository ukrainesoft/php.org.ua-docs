---
navigation:
  - intlbreakiterator.settext.md: '« IntlBreakIterator::setText'
  - intlrulebasedbreakiterator.construct.md: 'IntlRuleBasedBreakIterator::construct »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlRuleBasedBreakIterator
---
# Клас IntlRuleBasedBreakIterator

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Підклас [IntlBreakIterator](class.intlbreakiterator.md), який реалізує ітератор переривань ICU, чия поведінка задано набором правил. Це найчастіше використовуваний тип ітератора переривань.

Правила описані у розділі [» Руководство пользователя по анализу границ ICU](http://userguide.icu-project.org/boundaryanalysis#TOC-RBBI-Rules)

## Огляд класів

```classsynopsis

     
    

    
     
      class IntlRuleBasedBreakIterator
     

     
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

-   [IntlRuleBasedBreakIterator::construct](intlrulebasedbreakiterator.construct.md) - Створює ітератор на основі набору правил
-   [IntlRuleBasedBreakIterator::getBinaryRules](intlrulebasedbreakiterator.getbinaryrules.md) — Отримати бінарні дані зі скомпілованих правил
-   [IntlRuleBasedBreakIterator::getRules](intlrulebasedbreakiterator.getrules.md) — Отримати набір правил, які використовуються під час створення цього об'єкта
-   [IntlRuleBasedBreakIterator::getRuleStatus](intlrulebasedbreakiterator.getrulestatus.md) — Отримати найбільше значення статусу правил зупинки, що визначило поточну позицію зупинки
-   [IntlRuleBasedBreakIterator::getRuleStatusVec](intlrulebasedbreakiterator.getrulestatusvec.md) — отримати значення статусів із правил зупинки, які визначили поточну позицію зупинки
