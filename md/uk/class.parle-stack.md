---
navigation:
  - parle-rparser.validate.html: '« ParleRParser::validate'
  - parle-stack.pop.html: 'ParleStack::pop »'
  - index.html: PHP Manual
  - book.parle.html: Parle
title: Клас ParleStack
---
# Клас ParleStack

(PECL parle >= 0.7.0)

## Вступ

**ParleStack** - Це стек LIFO. Елементи додаються та видаляються лише з одного кінця.

## Огляд класів

```classsynopsis



    
     
      class Parle\Stack
     
     {


    /* Свойства */
    
     public
     bool
      $empty = true;

    public
     int
      $size = 0;

    public
     mixed
      $top;


    /* Методы */
    
   public pop(): void
public push(mixed $item): void

   }
```

## Властивості

empty

Чи є стек порожнім, лише читання.

size

Розмір стека тільки для читання.

top

Елемент на початку стеку.

## Зміст

-   [ParleStack::pop](parle-stack.pop.html) — Витягує предмет із стеку
-   [ParleStack::push](parle-stack.push.html) — Поміщає елемент у стек
