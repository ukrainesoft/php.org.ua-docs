Налаштування під час виконання

-   [« Установка](pgsql.installation.html)
    
-   [Типы ресурсов »](pgsql.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](pgsql.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації PostgreSQL**

| Имя                                                                                       | По умолчанию | Место изменения | Список изменений |
|-------------------------------------------------------------------------------------------|--------------|-----------------|------------------|
| [pgsql.allow\_persistent](pgsql.configuration.html#ini.pgsql.allow-persistent)            | "1"          | PHPINISYSTEM    |                  |
| [pgsql.max\_persistent](pgsql.configuration.html#ini.pgsql.max-persistent)                | "-1"         | PHPINISYSTEM    |                  |
| [pgsql.max\_links](pgsql.configuration.html#ini.pgsql.max-links)                          | "-1"         | PHPINISYSTEM    |                  |
| [pgsql.auto\_reset\_persistent](pgsql.configuration.html#ini.pgsql.auto-reset-persistent) | "0"          | PHPINISYSTEM    |                  |
| [pgsql.ignore\_notice](pgsql.configuration.html#ini.pgsql.ignore-notice)                  | "0"          | PHPINIALL       |                  |
| [pgsql.log\_notice](pgsql.configuration.html#ini.pgsql.log-notice)                        | "0"          | PHPINIALL       |                  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`pgsql.allow_persistent` bool

Чи слід дозволити постійне з'єднання з Postgres.

`pgsql.max_persistent` int

Максимальна кількість постійних з'єднань на один процес.

`pgsql.max_links` int

Максимальна кількість Postgres на один процес, включаючи постійні з'єднання.

`pgsql.auto_reset_persistent` int

Визначати розірвані постійні посилання з [pg\_pconnect()](function.pg-pconnect.html). Потрібні невеликі ресурси.

`pgsql.ignore_notice` int

Ігнорувати чи ні повідомлення від PostgreSQL.

`pgsql.log_notice` int

Чи записувати в лог повідомлення від PostgreSQL. Для запису в лог повідомлення також необхідно вимкнути PHP-директиву [pgsql.ignore\_notice](pgsql.configuration.html#ini.pgsql.ignore-notice)