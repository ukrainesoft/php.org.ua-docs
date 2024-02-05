---
navigation:
  - iconv.installation.md: « Встановлення
  - iconv.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - iconv.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції настроювання Iconv**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [iconv.input\_encoding](iconv.configuration.md#ini.iconv.input-encoding) | "" | **`INI_ALL`** | Застаріло з PHP 5.6.0. |
| [iconv.output\_encoding](iconv.configuration.md#ini.iconv.output-encoding) | "" | **`INI_ALL`** | Застаріло з PHP 5.6.0. |
| [iconv.internal\_encoding](iconv.configuration.md#ini.iconv.internal-encoding) | "" | **`INI_ALL`** | Застаріло з PHP 5.6.0. |

Коротке пояснення конфігураційних директив.

**Увага**

Деякі системи (наприклад, IBM AIX) використовують "ISO8859-1" замість "ISO-8859-1", тому це значення має бути вказано у налаштуваннях та параметрах функції.

`iconv.input_encoding`string

**Увага**

Ця можливість була оголошена *застарілої* починаючи з PHP 5.6.0. Вкрай не рекомендується покладатися на неї в майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість неї [input\_encoding](ini.core.md#ini.input-encoding)

`iconv.output_encoding`string

**Увага**

Ця можливість була оголошена *застарілої* починаючи з PHP 5.6.0. Вкрай не рекомендується покладатися на неї в майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість неї [output\_encoding](ini.core.md#ini.output-encoding)

`iconv.internal_encoding`string

**Увага**

Ця можливість була оголошена *застарілої* починаючи з PHP 5.6.0. Вкрай не рекомендується покладатися на неї в майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість неї [`default_charset`](ini.core.md#ini.default-charset)
