Налаштування під час виконання

-   [« Установка](mysql.installation.html)
    
-   [Типы ресурсов »](mysql.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](mysql.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Директиви конфігурації MySQL**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [mysql.allow\_local\_infile](mysql.configuration.html#ini.mysql.allow-local-infile) | "1" | PHPINISYSTEM |  |
| [mysql.allow\_persistent](mysql.configuration.html#ini.mysql.allow-persistent) | "1" | PHPINISYSTEM |  |
| [mysql.max\_persistent](mysql.configuration.html#ini.mysql.max-persistent) | "-1" | PHPINISYSTEM |  |
| [mysql.max\_links](mysql.configuration.html#ini.mysql.max-links) | "-1" | PHPINISYSTEM |  |
| [mysql.trace\_mode](mysql.configuration.html#ini.mysql.trace-mode) | "0" | PHPINIALL |  |
| [mysql.default\_port](mysql.configuration.html#ini.mysql.default-port) | NULL | PHPINIALL |  |
| [mysql.default\_socket](mysql.configuration.html#ini.mysql.default-socket) | NULL | PHPINIALL |  |
| [mysql.default\_host](mysql.configuration.html#ini.mysql.default-host) | NULL | PHPINIALL |  |
| [mysql.default\_user](mysql.configuration.html#ini.mysql.default-user) | NULL | PHPINIALL |  |
| [mysql.default\_password](mysql.configuration.html#ini.mysql.default-password) | NULL | PHPINIALL |  |
| [mysql.connect\_timeout](mysql.configuration.html#ini.mysql.connect-timeout) | "60" | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`mysql.allow_local_infile` int

Дозволяє доступ до локальних файлів з точки зору PHP за допомогою інструкцій LOAD DATA

`mysql.allow_persistent` bool

Чи дозволяти [постоянные соединения](features.persistent-connections.html) з MySQL.

`mysql.max_persistent` int

Максимальна кількість постійних з'єднань з MySQL на один процес.

`mysql.max_links` int

Максимальна кількість з'єднань з MySQL однією процес, включаючи постійні з'єднання.

`mysql.trace_mode` bool

Режим трасування. Якщо увімкнено опцію `mysql.trace_mode`, відображатимуться попередження при скануванні таблиць/індексів, непустих результуючих наборів (result sets), а також помилки SQL. (Додано у версії PHP 4.3.0)

`mysql.default_port` string

TCP-порт, який використовується для з'єднання з базою даних за замовчуванням (якщо не було вказано інше). Якщо ця директива опущена, порт буде взято зі змінного середовища MYSQLTCPPORT, значення `mysql-tcp` у файлі /etc/services або константи **`MYSQL_PORT`**, Вказаної при компіляції, у зазначеному порядку. Win32 використовує лише константу **`MYSQL_PORT`**

`mysql.default_socket` string

Ім'я стандартного сокету, що використовується для з'єднання з локальною базою даних, якщо не було вказано інше.

`mysql.default_host` string

Адреса сервера за промовчанням, що використовується для з'єднання з сервером бази даних, якщо не вказано іншу. Не працює в [SQL safe mode](ini.core.html#ini.sql.safe-mode)

`mysql.default_user` string

Стандартне ім'я користувача для з'єднання з сервером бази даних, якщо не вказано інше. Не працює в [SQL safe mode](ini.core.html#ini.sql.safe-mode)

`mysql.default_password` string

Стандартний пароль, який використовується для з'єднання з сервером бази даних, якщо не вказано інший. Не працює в [SQL safe mode](ini.core.html#ini.sql.safe-mode)

`mysql.connect_timeout` int

Час очікування на відповідь до розриву з'єднання в секундах. Linux також використовує це значення при очікуванні першої відповіді від сервера.