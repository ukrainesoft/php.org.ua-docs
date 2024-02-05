---
navigation:
  - intldatepatterngenerator.getbestpattern.md: '« IntlDatePatternGenerator::getBestPattern'
  - intlpartsiterator.getbreakiterator.md: 'IntlPartsIterator::getBreakIterator »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlPartsIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас IntlPartsIterator

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Об'єкти цього класу можна отримати з об'єктів [IntlBreakIterator](class.intlbreakiterator.md). Поки ітератор переривання надає послідовність обмежувачів, можна отримати **IntlPartsIterator** для зручності одержання текстових фрагментів між двома обмежувачами.

Ключі можуть бути зміщення від лівого або правого обмежувача або можуть бути просто послідовністю натуральних чисел. Дивіться [IntlBreakIterator::getPartsIterator()](intlbreakiterator.getpartsiterator.md)

## Огляд класів

```classsynopsis

    
     class IntlPartsIterator
    

    
     extends
      IntlIterator
     {

    /* Константы */
    
     public
     const
     int
      KEY_SEQUENTIAL;

    public
     const
     int
      KEY_LEFT;

    public
     const
     int
      KEY_RIGHT;


    /* Методы */
    
   public getBreakIterator(): IntlBreakIterator


    /* Наследуемые методы */
    public IntlIterator::current(): mixed
public IntlIterator::key(): mixed
public IntlIterator::next(): void
public IntlIterator::rewind(): void
public IntlIterator::valid(): bool

   }
```

## Обумовлені константи

**`IntlPartsIterator::KEY_SEQUENTIAL`**

**`IntlPartsIterator::KEY_LEFT`**

**`IntlPartsIterator::KEY_RIGHT`**

## Зміст

-   [IntlPartsIterator::getBreakIterator](intlpartsiterator.getbreakiterator.md)— Отримати IntlBreakIterator, зберігаючи ітератор цієї частини
