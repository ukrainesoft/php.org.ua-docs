---
navigation:
  - stomp.installation.md: « Встановлення
  - stomp.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - stomp.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [stomp.default\_broker](stomp.configuration.md#ini.stomp.default-broker) | tcp://localhost:61613 | **`INI_ALL`** |  |
| [stomp.default\_connection\_timeout\_sec](stomp.configuration.md#ini.stomp.default-connection-timeout-sec) |  | **`INI_ALL`** |  |
| [stomp.default\_connection\_timeout\_usec](stomp.configuration.md#ini.stomp.default-connection-timeout-usec) |  | **`INI_ALL`** |  |
| [stomp.default\_read\_timeout\_sec](stomp.configuration.md#ini.stomp.default-read-timeout-sec) |  | **`INI_ALL`** |  |
| [stomp.default\_read\_timeout\_usec](stomp.configuration.md#ini.stomp.default-read-timeout-usec) |  | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`stomp.default_broker`string

За замовчуванням брокер URI використовується при підключенні до брокера повідомлень, якщо інші URI не вказані.

`stomp.default_connection_timeout_sec`int

Секундна частина часу очікування підключення за промовчанням.

`stomp.default_connection_timeout_usec`int

Мікросекундна частина часу очікування підключення за промовчанням.

`stomp.default_read_timeout_sec`int

Секундна частина часу очікування за промовчанням.

`stomp.default_read_timeout_usec`int

Мікросекундна частина часу очікування за промовчанням.
