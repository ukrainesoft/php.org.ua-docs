---
navigation:
  - mysql.installation.md: « Встановлення
  - mysql.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - mysql.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Директиви конфігурації MySQL**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [mysql.allow\_local\_infile](mysql.configuration.md#ini.mysql.allow-local-infile) | "1" | **`INI_SYSTEM`** |  |
| [mysql.allow\_persistent](mysql.configuration.md#ini.mysql.allow-persistent) | "1" | **`INI_SYSTEM`** |  |
| [mysql.max\_persistent](mysql.configuration.md#ini.mysql.max-persistent) | "-1" | **`INI_SYSTEM`** |  |
| [mysql.max\_links](mysql.configuration.md#ini.mysql.max-links) | "-1" | **`INI_SYSTEM`** |  |
| [mysql.trace\_mode](mysql.configuration.md#ini.mysql.trace-mode) | "0" | **`INI_ALL`** |  |
| [mysql.default\_port](mysql.configuration.md#ini.mysql.default-port) | NULL | **`INI_ALL`** |  |
| [mysql.default\_socket](mysql.configuration.md#ini.mysql.default-socket) | NULL | **`INI_ALL`** |  |
| [mysql.default\_host](mysql.configuration.md#ini.mysql.default-host) | NULL | **`INI_ALL`** |  |
| [mysql.default\_user](mysql.configuration.md#ini.mysql.default-user) | NULL | **`INI_ALL`** |  |
| [mysql.default\_password](mysql.configuration.md#ini.mysql.default-password) | NULL | **`INI_ALL`** |  |
| [mysql.connect\_timeout](mysql.configuration.md#ini.mysql.connect-timeout) | "60" | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`mysql.allow_local_infile`int

Дозволяє доступ до локальних файлів з точки зору PHP за допомогою інструкцій LOAD DATA

`mysql.allow_persistent`bool

Чи дозволяти [постійні з'єднання](features.persistent-connections.md) з MySQL.

`mysql.max_persistent`int

Максимальна кількість постійних з'єднань з MySQL на один процес.

`mysql.max_links`int

Максимальна кількість з'єднань з MySQL однією процес, включаючи постійні з'єднання.

`mysql.trace_mode`bool

Режим трасування. Якщо увімкнено опцію `mysql.trace_mode`, відображатимуться попередження при скануванні таблиць/індексів, непустих результуючих наборів (result sets), а також помилки SQL. (Додано у версії PHP 4.3.0)

`mysql.default_port`string

TCP-порт, який використовується для з'єднання з базою даних за промовчанням (якщо не було вказано інше). Якщо ця директива опущена, порт буде взято зі змінного середовища MYSQL\_TCP\_PORT, значения`mysql-tcp` у файлі /etc/services або константи **`MYSQL_PORT`**, Вказаної при компіляції, у зазначеному порядку. Win32 використовує лише константу **`MYSQL_PORT`**

`mysql.default_socket`string

Ім'я стандартного сокету, що використовується для з'єднання з локальною базою даних, якщо не було вказано інше.

`mysql.default_host`string

Адреса сервера за промовчанням, що використовується для з'єднання з сервером бази даних, якщо не вказано іншу. Не працює в [SQL safe mode](ini.core.md#ini.sql.safe-mode)

`mysql.default_user`string

Стандартне ім'я користувача для з'єднання з сервером бази даних, якщо не вказано інше. Не працює в [SQL safe mode](ini.core.md#ini.sql.safe-mode)

`mysql.default_password`string

Стандартний пароль, який використовується для підключення до сервера бази даних, якщо не вказано інший. Не працює в [SQL safe mode](ini.core.md#ini.sql.safe-mode)

`mysql.connect_timeout`int

Час очікування на відповідь до розриву з'єднання в секундах. Linux також використовує це значення при очікуванні першої відповіді від сервера.
