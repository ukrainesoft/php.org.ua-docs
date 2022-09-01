---
navigation:
  - class.parle-token.html: « ParleToken
  - class.parle-lexerexception.html: ParleLexerException »
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас ParleErrorInfo
---
# Клас ParleErrorInfo

(PECL parle >= 0.5.2)

## Вступ

Клас надає детальну інформацію про помилку, надану [ParleParser::errorInfo()](parle-parser.errorinfo.html)

## Огляд класів

```synopsis



    
     
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

ід

Ідентифікатор помилки.

position

Позиція, де сталася помилка.

token

Якщо можна застосувати - [ParleToken](class.parle-token.html), пов'язаний з помилкою, в іншому випадку **`null`**
