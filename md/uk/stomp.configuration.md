Налаштування під час виконання

-   [« Установка](stomp.installation.html)
    
-   [Типы ресурсов »](stomp.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](stomp.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [stomp.default\_broker](stomp.configuration.html#ini.stomp.default-broker) | tcp://localhost:61613 | PHPINIALL |  |
| [stomp.default\_connection\_timeout\_sec](stomp.configuration.html#ini.stomp.default-connection-timeout-sec) |  | PHPINIALL |  |
| [stomp.default\_connection\_timeout\_usec](stomp.configuration.html#ini.stomp.default-connection-timeout-usec) |  | PHPINIALL |  |
| [stomp.default\_read\_timeout\_sec](stomp.configuration.html#ini.stomp.default-read-timeout-sec) |  | PHPINIALL |  |
| [stomp.default\_read\_timeout\_usec](stomp.configuration.html#ini.stomp.default-read-timeout-usec) |  | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`stomp.default_broker` string

За замовчуванням брокер URI використовується при підключенні до брокера повідомлень, якщо інші URI не вказані.

`stomp.default_connection_timeout_sec` int

Секундна частина часу очікування підключення за промовчанням.

`stomp.default_connection_timeout_usec` int

Мікросекундна частина часу очікування підключення за промовчанням.

`stomp.default_read_timeout_sec` int

Секундна частина часу очікування зчитування за промовчанням.

`stomp.default_read_timeout_usec` int

Мікросекундна частина часу очікування за промовчанням.