Клас ParleToken

-   [« Parle\\Stack::push](parle-stack.push.html)
    
-   [Parle\\ErrorInfo »](class.parle-errorinfo.html)
    
-   [PHP Manual](index.html)
    
-   [Parle](book.parle.html)
    
-   Клас ParleToken
    

# Клас ParleToken

(PECL parle >= 0.5.2)

## Вступ

Клас представляє токен. Лексер повертає екземпляри цього класу.

## Огляд класів

```synopsis



    
     
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

ід

Ідентифікатор токена.

value

Значення токена.

## Обумовлені константи

**`Parle\Token::EOI`**

Кінець вхідного ідентифікатора токена.

**`Parle\Token::UNKNOWN`**

Невідомий ідентифікатор токену.

**`Parle\Token::SKIP`**

Пропустіть ідентифікатор токена.