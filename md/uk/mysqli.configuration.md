---
navigation:
  - mysqli.installation.md: « Встановлення
  - mysqli.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - mysqli.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації MySQLi**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [mysqli.allow\_local\_infile](mysqli.configuration.md#ini.mysqli.allow-local-infile) | "0" | **`INI_SYSTEM`** | До PHP 7.2.16 та 7.3.3 значенням за умовчанням було "1". |
| [mysqli.local\_infile\_directory](mysqli.configuration.md#ini.mysqli.local-infile-directory) |  | **`INI_SYSTEM`** | Доступно з PHP 8.1.0. |
| [mysqli.allow\_persistent](mysqli.configuration.md#ini.mysqli.allow-persistent) | "1" | **`INI_SYSTEM`** |  |
| [mysqli.max\_persistent](mysqli.configuration.md#ini.mysqli.max-persistent) | "-1" | **`INI_SYSTEM`** |  |
| [mysqli.max\_links](mysqli.configuration.md#ini.mysqli.max-links) | "-1" | **`INI_SYSTEM`** |  |
| [mysqli.default\_port](mysqli.configuration.md#ini.mysqli.default-port) | "3306" | **`INI_ALL`** |  |
| [mysqli.default\_socket](mysqli.configuration.md#ini.mysqli.default-socket) | NULL | **`INI_ALL`** |  |
| [mysqli.default\_host](mysqli.configuration.md#ini.mysqli.default-host) | NULL | **`INI_ALL`** |  |
| [mysqli.default\_user](mysqli.configuration.md#ini.mysqli.default-user) | NULL | **`INI_ALL`** |  |
| [mysqli.default\_pw](mysqli.configuration.md#ini.mysqli.default-pw) | NULL | **`INI_ALL`** |  |
| [mysqli.reconnect](mysqli.configuration.md#ini.mysqli.reconnect) | "0" | **`INI_SYSTEM`** | Видалено, починаючи з PHP 8.2.0 |
| [mysqli.rollback\_on\_cached\_plink](mysqli.configuration.md#ini.mysqli.rollback-on-cached-plink) | "0" | **`INI_SYSTEM`** |  |

Інші деталі та визначення констант INI\_\*смотрите в разделе[конфігураційні зміни](configuration.changes.md)

Коротке пояснення конфігураційних директив.

`mysqli.allow_local_infile`int

Дозволяє доступ до локальних файлів з точки зору PHP за допомогою інструкцій LOAD DATA.

`mysqli.local_infile_directory`string

Дозволяє обмежити завантаження LOAD DATA файлами, розташованими у вказаному каталозі.

`mysqli.allow_persistent`int

Включає можливість створювати постійні з'єднання за допомогою [mysqli\_connect()](function.mysqli-connect.md)

`mysqli.max_persistent`int

Максимально можлива кількість постійних з'єднань. Для необмеженої кількості встановіть 0.

`mysqli.max_links`int

Максимальна кількість з'єднань MySQL на процес.

`mysqli.default_port`int

TCP-порт, який використовується за умовчанням для з'єднання з сервером баз даних, якщо інше значення не вказано. Якщо значення за промовчанням не вказано, воно буде отримано зі змінного середовища оточення `MYSQL_TCP_PORT`, директиви `mysql-tcp` у файлі /etc/services або константи `MYSQL_PORT`, яка задається під час компіляції, у вказаному порядку. Win32 використовує лише константу `MYSQL_PORT`

`mysqli.default_socket`string

Ім'я стандартного сокету, яке використовується для з'єднання з локальною базою даних, якщо ім'я сокета не було вказано явно.

`mysqli.default_host`string

Ім'я сервера, яке використовується, якщо ім'я не було вказано.

`mysqli.default_user`string

Ім'я користувача за промовчанням, якщо ім'я не було вказано явно.

`mysqli.default_pw`string

Пароль, який використовується за замовчуванням для підключення до бази даних, якщо пароль не був явно вказаний.

`mysqli.reconnect`int

Автоматично відновлювати з'єднання за його втрати.

> **Зауваження**: Ця установка ігнорується драйвером "mysqlnd" і була видалена в PHP 8.2.0.

`mysqli.rollback_on_cached_plink`bool

Якщо цей параметр увімкнено, закриття постійного з'єднання відкотить будь-які транзакції цього з'єднання, що очікують, перш ніж воно буде повернено в пул постійних з'єднань. В іншому випадку очікуючі з'єднання будуть відкочуватися тільки тоді, коли з'єднання повторно використане або коли воно буде фактично закрите.

Користувачі не можуть встановлювати `MYSQL_OPT_READ_TIMEOUT` за допомогою API-дзвінків або встановлення конфігураційних значень під час роботи скрипту. Врахуйте, що якби це було можливо, то `libmysqlclient` і потоки по-різному обробляли б значення `MYSQL_OPT_READ_TIMEOUT`
