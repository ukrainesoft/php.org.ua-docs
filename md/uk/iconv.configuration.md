---
navigation:
  - iconv.installation.md: « Установка
  - iconv.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - iconv.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції настроювання Iconv**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [iconv.inputencoding](iconv.configuration.html#ini.iconv.input-encoding) | "" | PHPINIALL | Застаріло з PHP 5.6.0. |
| [iconv.outputencoding](iconv.configuration.html#ini.iconv.output-encoding) | "" | PHPINIALL | Застаріло з PHP 5.6.0. |
| [iconv.internalencoding](iconv.configuration.html#ini.iconv.internal-encoding) | "" | PHPINIALL | Застаріло з PHP 5.6.0. |

Коротке пояснення конфігураційних директив.

**Увага**

Деякі системи (наприклад, IBM AIX) використовують "ISO8859-1" замість "ISO-8859-1", тому це значення має бути вказано у налаштуваннях та параметрах функції.

`iconv.input_encoding` string

**Увага**

Ця можливість була оголошена *застарілої*починаючи з PHP 5.6.0. Вкрай не рекомендується покладатися на цю можливість у майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість неї [inputencoding](ini.core.html#ini.input-encoding)

`iconv.output_encoding` string

**Увага**

Ця можливість була оголошена *застарілої*починаючи з PHP 5.6.0. Вкрай не рекомендується покладатися на цю можливість у майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість неї [outputencoding](ini.core.html#ini.output-encoding)

`iconv.internal_encoding` string

**Увага**

Ця можливість була оголошена *застарілої*починаючи з PHP 5.6.0. Вкрай не рекомендується покладатися на цю можливість у майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість неї [`default_charset`](ini.core.html#ini.default-charset)
