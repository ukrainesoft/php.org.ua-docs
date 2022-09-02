---
navigation:
  - stomp.installation.md: « Установка
  - stomp.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - stomp.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [stomp.defaultbroker](stomp.configuration.md#ini.stomp.default-broker) | tcp://localhost:61613 | PHPINIALL |  |
| [stomp.defaultconnectiontimeoutsec](stomp.configuration.md#ini.stomp.default-connection-timeout-sec) |  | PHPINIALL |  |
| [stomp.defaultconnectiontimeoutusec](stomp.configuration.md#ini.stomp.default-connection-timeout-usec) |  | PHPINIALL |  |
| [stomp.defaultreadtimeoutsec](stomp.configuration.md#ini.stomp.default-read-timeout-sec) |  | PHPINIALL |  |
| [stomp.defaultreadtimeoutusec](stomp.configuration.md#ini.stomp.default-read-timeout-usec) |  | PHPINIALL |  |

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
