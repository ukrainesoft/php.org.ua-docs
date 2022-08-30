Клас StompFrame

-   [« Stomp::unsubscribe](stomp.unsubscribe.html)
    
-   [StompFrame::construct »](stompframe.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Stomp](book.stomp.html)
    
-   Клас StompFrame
    

# Клас StompFrame

(PECL stomp >= 0.1.0)

## Вступ

Показує повідомлення, яке було надіслано або отримано від Stomp-сумісного брокера повідомлень (Message Broker).

## Огляд класів

```synopsis



    
     
      class StompFrame
     
     {

    /* Свойства */
    
     public
      $command;

    public
      $headers;

    public
      $body;



    /* Методы */
    
   __construct(string $command = ?, array $headers = ?, string $body = ?)

   }
```

## Властивості

command

Команда кадру.

headers

Заголовки кадру (array).

body

Тіло кадру.

## Зміст

-   [StompFrame::construct](stompframe.construct.html) - Конструктор