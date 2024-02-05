---
navigation:
  - class.parle-token.md: « Parle\\Token
  - class.parle-lexerexception.md: Parle\\LexerException »
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас Parle\\ErrorInfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Parle\\ErrorInfo

(PECL parle >= 0.5.2)

## Вступ

Класс представляет подробную информацию об ошибке, предоставленной[Parle\\Parser::errorInfo()](parle-parser.errorinfo.md)

## Огляд класів

```classsynopsis



    
     
      class Parle\ErrorInfo
     
     {

    /* Свойства */
    
     public
     int
      $id;

    public
     int
      $position;

    public
     mixed
      $token;



    /* Методы */
    
    
   }
```

## Властивості

id

Ідентифікатор помилки.

position

Позиція, де сталася помилка.

token

Якщо можна застосувати - [Parle\\Token](class.parle-token.md), пов'язаний з помилкою, в іншому випадку **`null`**
