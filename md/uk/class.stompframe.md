---
navigation:
  - stomp.unsubscribe.md: '« Stomp::unsubscribe'
  - stompframe.construct.md: 'StompFrame::\_\_construct »'
  - index.md: PHP Manual
  - book.stomp.md: Stomp
title: Клас StompFrame
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас StompFrame

(PECL stomp >= 0.1.0)

## Вступ

Показує повідомлення, яке було надіслано або отримано від Stomp-сумісного брокера повідомлень (Message Broker).

## Огляд класів

```classsynopsis



    
     
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

-   [StompFrame::\_\_construct](stompframe.construct.md) \- Конструктор
