- [« Установка](iconv.installation.md)
- [Типи ресурсів»](iconv.resources.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](iconv.setup.md)
- Налаштування під час виконання

## Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

| Ім'я За замовчуванням                                                         | Місце зміни | Список змін |
| ----------------------------------------------------------------------------- | ----------- | ----------- |
| [iconv.input_encoding](iconv.configuration.md#ini.iconv.input-encoding)       | ""          | PHP_INI_ALL | Застаріло з PHP 5.6.0.
| [iconv.output_encoding](iconv.configuration.md#ini.iconv.output-encoding)     | ""          | PHP_INI_ALL | Застаріло з PHP 5.6.0.
| [iconv.internal_encoding](iconv.configuration.md#ini.iconv.internal-encoding) | ""          | PHP_INI_ALL | Застаріло з PHP 5.6.0.

**Опції налаштування Iconv**

Коротке пояснення конфігураційних директив.

**Увага**

Деякі системи (наприклад, IBM AIX) використовують "ISO8859-1" замість
"ISO-8859-1", тому це значення має бути вказано в налаштуваннях та
параметри функції.

`iconv.input_encoding` string
**Увага**
Ця можливість була оголошена *УСТАРНІЙ*, починаючи з PHP 5.6.0.
Вкрай не рекомендується покладатися на цю можливість у майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість
її [input_encoding](ini.core.md#ini.input-encoding).

`iconv.output_encoding` string
**Увага**
Ця можливість була оголошена *УСТАРНІЙ*, починаючи з PHP 5.6.0.
Вкрай не рекомендується покладатися на цю можливість у майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість
її [output_encoding](ini.core.md#ini.output-encoding).

`iconv.internal_encoding` string
**Увага**
Ця можливість була оголошена *УСТАРНІЙ*, починаючи з PHP 5.6.0.
Вкрай не рекомендується покладатися на цю можливість у майбутньому.

У PHP 5.6 і більше потрібно залишати цю опцію порожньою і використовувати замість
її [`default_charset`](ini.core.md#ini.default-charset).
