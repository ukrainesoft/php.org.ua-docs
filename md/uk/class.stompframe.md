---
navigation:
  - stomp.unsubscribe.html: '« Stomp::unsubscribe'
  - stompframe.construct.html: 'StompFrame::construct »'
  - index.html: PHP Manual
  - book.stomp.html: Stomp
title: Клас StompFrame
---
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

-   [StompFrame::construct](stompframe.construct.md) - Конструктор
