- [« Stomp::unsubscribe](stomp.unsubscribe.md)
- [StompFrame::\_\_construct »](stompframe.construct.md)

- [PHP Manual](index.md)
- [Stomp](book.stomp.md)
- Клас StompFrame

# Клас StompFrame

(PECL stomp \>= 0.1.0)

## Вступ

Представляє повідомлення, яке було надіслано або отримано від
Stomp-сумісного брокера повідомлень (Message Broker).

## Огляд класів

class **StompFrame** {

/\* Властивості \*/

public `$command`;

public `$headers`;

public `$body`;

/\* Методи \*/

[\_\_construct](stompframe.construct.md)(string `$command` = ?, array
`$headers` = ?, string `$body` = ?)

}

## Властивості

`command`
Команда кадру.

`headers`
Заголовки кадру (array).

`body`
Тіло кадру.

## Зміст

- [StompFrame::\_\_construct](stompframe.construct.md) - Конструктор
