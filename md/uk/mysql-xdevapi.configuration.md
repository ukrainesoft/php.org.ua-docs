Налаштування під час виконання

-   [« Установка](mysql-xdevapi.installation.html)
    
-   [Сборка / Компиляция из исходного кода »](mysql-xdevapi.build.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](mysql-xdevapi.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Mysqlxdevapi**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [xmysqlnd.collect\_memory\_statistics](mysql-xdevapi.configuration.html#ini.xmysqlnd.collect-memory-statistics) |  | PHPINISYSTEM |  |
| [xmysqlnd.collect\_statistics](mysql-xdevapi.configuration.html#ini.xmysqlnd.collect-statistics) |  | PHPINIALL |  |
| [xmysqlnd.debug](mysql-xdevapi.configuration.html#ini.xmysqlnd.debug) |  | PHPINISYSTEM |  |
| [xmysqlnd.mempool\_default\_size](mysql-xdevapi.configuration.html#ini.xmysqlnd.mempool-default-size) |  | PHPINIALL |  |
| [xmysqlnd.net\_read\_timeout](mysql-xdevapi.configuration.html#ini.xmysqlnd.net-read-timeout) |  | PHPINISYSTEM |  |
| [xmysqlnd.trace\_alloc](mysql-xdevapi.configuration.html#ini.xmysqlnd.trace-alloc) |  | PHPINISYSTEM |  |

Коротке пояснення конфігураційних директив.

`xmysqlnd.collect_memory_statistics` int

`xmysqlnd.collect_statistics` int

`xmysqlnd.debug` string

`xmysqlnd.mempool_default_size` int

`xmysqlnd.net_read_timeout` int

`xmysqlnd.trace_alloc` string