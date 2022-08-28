Клас ParleStack

-   [« Parle\\RParser::validate](parle-rparser.validate.html)
    
-   [Parle\\Stack::pop »](parle-stack.pop.html)
    
-   [PHP Manual](index.html)
    
-   [Parle](book.parle.html)
    
-   Клас ParleStack
    

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

-   [Parle\\Stack::pop](parle-stack.pop.html) — Витягує предмет із стеку
-   [Parle\\Stack::push](parle-stack.push.html) — Поміщає елемент у стек