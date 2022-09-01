---
navigation:
  - yar.installation.md: « Установка
  - yar.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yar.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Yar Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yar.packager](yar.configuration.html#ini.yar.packager) | php | PHPINISYSTEM |  |
| [yar.debug](yar.configuration.html#ini.yar.debug) | Off | PHPINIALL |  |
| [yar.connecttimeout](yar.configuration.html#ini.yar.connect-timeout) |  | PHPINIALL |  |
| [yar.timeout](yar.configuration.html#ini.yar.timeout) |  | PHPINIALL |  |
| [yar.exposeinfo](yar.configuration.html#ini.yar.expose-info) | Він | PHPINISYSTEM |  |

Коротке пояснення конфігураційних директив.

`yar.packager` string

може бути php, json та msgpack (потрібна вбудована підтримка msgpack)

`yar.debug` string

`yar.connect_timeout` int

Час очікування з'єднання у мілісекундах.

`yar.timeout` int

Час очікування у мілісекундах.

`yar.expose_info` bool

чи розкривати дані сервера (при доступі за допомогою GET)
