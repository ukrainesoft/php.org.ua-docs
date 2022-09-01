---
navigation:
  - intldatepatterngenerator.getbestpattern.html: '« IntlDatePatternGenerator::getBestPattern'
  - intlpartsiterator.getbreakiterator.html: 'IntlPartsIterator::getBreakIterator »'
  - index.html: PHP Manual
  - book.intl.html: intl
title: Клас IntlPartsIterator
---
# Клас IntlPartsIterator

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Об'єкти цього класу можна отримати з об'єктів [IntlBreakIterator](class.intlbreakiterator.md). Поки ітератор переривання надає послідовність обмежувачів, можна отримати **IntlPartsIterator** для зручності одержання текстових фрагментів між двома обмежувачами.

Ключі можуть бути зміщення від лівого або правого обмежувача або можуть бути просто послідовністю натуральних чисел. Дивіться [IntlBreakIterator::getPartsIterator()](intlbreakiterator.getpartsiterator.md)

## Огляд класів

```classsynopsis

     
    

    
     
      class IntlPartsIterator
     

     
      extends
       IntlIterator
     
     {

    /* Constants */
    
     const
     int
      KEY_SEQUENTIAL = 0;

    const
     int
      KEY_LEFT = 1;

    const
     int
      KEY_RIGHT = 2;


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

-   [IntlPartsIterator::getBreakIterator](intlpartsiterator.getbreakiterator.md) — Отримати IntlBreakIterator, зберігаючи ітератор цієї частини
