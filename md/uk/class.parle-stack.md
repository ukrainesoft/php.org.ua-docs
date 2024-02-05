---
navigation:
  - parle-rparser.validate.md: '« Parle\\RParser::validate'
  - parle-stack.pop.md: 'Parle\\Stack::pop »'
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас Parle\\Stack
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Parle\\Stack

(PECL parle >= 0.7.0)

## Вступ

**Parle\\Stack** - Це стек LIFO. Елементи додаються та видаляються лише з одного кінця.

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

Чи є стек порожнім, тільки для читання.

size

Розмір стека тільки для читання.

top

Елемент на початку стеку.

## Зміст

-   [Parle\\Stack::pop](parle-stack.pop.md)— Витягує предмет із стеку
-   [Parle\\Stack::push](parle-stack.push.md)— Поміщає елемент у стек
