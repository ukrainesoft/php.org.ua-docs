Клас IntlIterator

-   [« IntlException](class.intlexception.html)
    
-   [IntlIterator::current »](intliterator.current.html)
    
-   [PHP Manual](index.html)
    
-   [intl](book.intl.html)
    
-   Клас IntlIterator
    

# Клас IntlIterator

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Цей клас представляє ітератор об'єктів модуля intl у випадках, коли не можна призначити будь-який інший ітератор для об'єкта даного модуля. Єдиний об'єкт ітератора для використання в [конструкції `foreach`](control-structures.foreach.html) може бути отриманий тільки (у відповідній частині тут) з об'єктів, тому об'єкти даного класу служать для отримання таких внутрішніх об'єктів. Для зручності цей клас також реалізує інтерфейс. [Iterator](class.iterator.html), дозволяючи взаємодіяти з колекціями значень використовуючи методи, визначені в цьому інтерфейсі. Обидва ці методи і внутрішні об'єкти ітератора зберігають свій стан під час передачі в `foreach`. (Тобто внутрішній покажчик і поточне значення залишаються незмінними).

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

-   [IntlIterator::current](intliterator.current.html) — Отримати поточний елемент
-   [IntlIterator::key](intliterator.key.html) — Отримати ключ поточного елемента
-   [IntlIterator::next](intliterator.next.html) — Перейти до наступного елементу
-   [IntlIterator::rewind](intliterator.rewind.html) — Перейти до першого елементу
-   [IntlIterator::valid](intliterator.valid.html) — Перевірити, чи поточна позиція коректна