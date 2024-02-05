---
navigation:
  - class.intlexception.md: « IntlException
  - intliterator.current.md: 'IntlIterator::current »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас IntlIterator

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Цей клас представляє ітератор об'єктів модуля intl у випадках, коли не можна призначити будь-який інший ітератор для об'єкта даного модуля. Єдиний об'єкт ітератора для використання в [конструкції `foreach`](control-structures.foreach.md) може бути отриманий тільки (у відповідній частині тут) з об'єктів, тому об'єкти даного класу служать для отримання таких внутрішніх об'єктів. Для зручності цей клас також реалізує інтерфейс. [Iterator](class.iterator.md), дозволяючи взаємодіяти з колекціями значень використовуючи методи, визначені в цьому інтерфейсі. Обидва ці методи і внутрішні об'єкти ітератора зберігають свій стан під час передачі в `foreach`. (Тобто внутрішній покажчик і поточне значення залишаються незмінними).

Класи нащадки можуть надавати ширшу функціональність.

## Огляд класів

```classsynopsis

    
     class IntlIterator
    

    
     implements
      Iterator {

    /* Методы */
    
   public current(): mixed
public key(): mixed
public next(): void
public rewind(): void
public valid(): bool

   }
```

## Зміст

-   [IntlIterator::current](intliterator.current.md)— Отримати поточний елемент
-   [IntlIterator::key](intliterator.key.md)— Отримати ключ поточного елемента
-   [IntlIterator::next](intliterator.next.md)— Перейти до наступного елементу
-   [IntlIterator::rewind](intliterator.rewind.md)— Перейти до першого елементу
-   [IntlIterator::valid](intliterator.valid.md)— Перевірити, чи поточна позиція коректна
