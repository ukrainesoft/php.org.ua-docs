---
navigation:
  - pgsql.installation.md: « Установка
  - pgsql.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - pgsql.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації PostgreSQL**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [pgsql.allowpersistent](pgsql.configuration.md#ini.pgsql.allow-persistent) | "1" | PHPINISYSTEM |  |
| [pgsql.maxpersistent](pgsql.configuration.md#ini.pgsql.max-persistent) | "-1" | PHPINISYSTEM |  |
| [pgsql.maxlinks](pgsql.configuration.md#ini.pgsql.max-links) | "-1" | PHPINISYSTEM |  |
| [pgsql.autoresetpersistent](pgsql.configuration.md#ini.pgsql.auto-reset-persistent) | "0" | PHPINISYSTEM |  |
| [pgsql.ignorenotice](pgsql.configuration.md#ini.pgsql.ignore-notice) | "0" | PHPINIALL |  |
| [pgsql.lognotice](pgsql.configuration.md#ini.pgsql.log-notice) | "0" | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`pgsql.allow_persistent` bool

Чи слід дозволити постійне з'єднання з Postgres.

`pgsql.max_persistent` int

Максимальна кількість постійних з'єднань на один процес.

`pgsql.max_links` int

Максимальна кількість Postgres на один процес, включаючи постійні з'єднання.

`pgsql.auto_reset_persistent` int

Визначати розірвані постійні посилання з [пгpconnect()](function.pg-pconnect.md). Потрібні невеликі ресурси.

`pgsql.ignore_notice` int

Ігнорувати чи ні повідомлення від PostgreSQL.

`pgsql.log_notice` int

Чи записувати в лог повідомлення від PostgreSQL. Для запису в лог повідомлення також необхідно вимкнути PHP-директиву [pgsql.ignorenotice](pgsql.configuration.md#ini.pgsql.ignore-notice)
