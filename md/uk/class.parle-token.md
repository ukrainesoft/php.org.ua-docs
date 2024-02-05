---
navigation:
  - parle-stack.push.md: '« Parle\\Stack::push'
  - class.parle-errorinfo.md: Parle\\ErrorInfo »
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас Parle\\Token
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Parle\\Token

(PECL parle >= 0.5.2)

## Вступ

Клас представляє токен. Лексер повертає екземпляри цього класу.

## Огляд класів

```classsynopsis



    
     
      class Parle\Token
     
     {

    /* Constants */
    
     const
     int
      EOI = 0;

    const
     int
      UNKNOWN = -1;

    const
     int
      SKIP = -2;


    /* Свойства */
    public
     int
      $id;

    public
     string
      $value;



    /* Методы */
    
    
   }
```

## Властивості

id

Ідентифікатор токена.

value

Значення токена.

## Обумовлені константи

**`Parle\Token::EOI`**

Кінець вхідного ідентифікатора токена.

**`Parle\Token::UNKNOWN`**

Невідомий ідентифікатор токену.

**`Parle\Token::SKIP`**

Пропустити ідентифікатор токена.
