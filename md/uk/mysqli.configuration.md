Налаштування під час виконання

-   [« Установка](mysqli.installation.html)
    
-   [Типы ресурсов »](mysqli.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](mysqli.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації MySQLi**

| Имя                                                                                                 | По умолчанию | Место изменения | Список изменений                                         |
|-----------------------------------------------------------------------------------------------------|--------------|-----------------|----------------------------------------------------------|
| [mysqli.allow\_local\_infile](mysqli.configuration.html#ini.mysqli.allow-local-infile)              | "0"          | PHPINISYSTEM    | До PHP 7.2.16 та 7.3.3 значенням за умовчанням було "1". |
| [mysqli.local\_infile\_directory](mysqli.configuration.html#ini.mysqli.local-infile-directory)      |              | PHPINISYSTEM    | Доступно з PHP 8.1.0.                                    |
| [mysqli.allow\_persistent](mysqli.configuration.html#ini.mysqli.allow-persistent)                   | "1"          | PHPINISYSTEM    |                                                          |
| [mysqli.max\_persistent](mysqli.configuration.html#ini.mysqli.max-persistent)                       | "-1"         | PHPINISYSTEM    |                                                          |
| [mysqli.max\_links](mysqli.configuration.html#ini.mysqli.max-links)                                 | "-1"         | PHPINISYSTEM    |                                                          |
| [mysqli.default\_port](mysqli.configuration.html#ini.mysqli.default-port)                           | "3306"       | PHPINIALL       |                                                          |
| [mysqli.default\_socket](mysqli.configuration.html#ini.mysqli.default-socket)                       | NULL         | PHPINIALL       |                                                          |
| [mysqli.default\_host](mysqli.configuration.html#ini.mysqli.default-host)                           | NULL         | PHPINIALL       |                                                          |
| [mysqli.default\_user](mysqli.configuration.html#ini.mysqli.default-user)                           | NULL         | PHPINIALL       |                                                          |
| [mysqli.default\_pw](mysqli.configuration.html#ini.mysqli.default-pw)                               | NULL         | PHPINIALL       |                                                          |
| [mysqli.reconnect](mysqli.configuration.html#ini.mysqli.reconnect)                                  | "0"          | PHPINISYSTEM    |                                                          |
| [mysqli.rollback\_on\_cached\_plink](mysqli.configuration.html#ini.mysqli.rollback-on-cached-plink) | "0"          | PHPINISYSTEM    |                                                          |

Інші деталі та визначення констант PHPINI дивіться у розділі [конфигурационные изменения](configuration.changes.html)

Коротке пояснення конфігураційних директив.

`mysqli.allow_local_infile` int

Дозволяє доступ до локальних файлів з точки зору PHP за допомогою інструкцій LOAD DATA.

`mysqli.local_infile_directory` string

Дозволяє обмежити завантаження LOAD DATA файлами, розташованими у вказаному каталозі.

`mysqli.allow_persistent` int

Включає можливість створювати постійні з'єднання за допомогою [mysqli\_connect()](function.mysqli-connect.html)

`mysqli.max_persistent` int

Максимально можлива кількість постійних з'єднань. Для необмеженої кількості встановіть 0.

`mysqli.max_links` int

Максимальна кількість MySQL з'єднань на процес.

`mysqli.default_port` int

TCP-порт, що використовується за замовчуванням для з'єднання з сервером баз даних, якщо інше значення не вказано. Якщо значення за промовчанням не вказано, воно буде отримано зі змінного середовища оточення `MYSQL_TCP_PORT`, директиви `mysql-tcp` у файлі /etc/services або константи `MYSQL_PORT`, яка задається під час компіляції, у вказаному порядку. Win32 використовує лише константу `MYSQL_PORT`

`mysqli.default_socket` string

Ім'я стандартного сокета, яке використовується для з'єднання з локальною базою даних, якщо ім'я сокета не було вказано явно.

`mysqli.default_host` string

Ім'я сервера, яке використовується, якщо ім'я не було вказано.

`mysqli.default_user` string

Ім'я користувача за промовчанням, якщо ім'я не було вказано явно.

`mysqli.default_pw` string

Пароль, який використовується за замовчуванням для підключення до бази даних, якщо пароль не був явно вказаний.

`mysqli.reconnect` int

Автоматично відновлювати з'єднання за його втрати.

> **Зауваження**: Ця установка ігнорується драйвером "mysqlnd".

`mysqli.rollback_on_cached_plink` bool

Якщо цей параметр увімкнено, закриття постійного з'єднання відкотить будь-які транзакції цього з'єднання, що очікують, перш ніж воно буде повернено в пул постійних з'єднань. В іншому випадку очікуючі з'єднання будуть відкочуватися тільки тоді, коли з'єднання повторно використане або коли воно буде фактично закрите.

Користувачі не можуть встановлювати `MYSQL_OPT_READ_TIMEOUT` за допомогою API-дзвінків або встановлення конфігураційних значень під час роботи скрипту. Врахуйте, що якби це було можливо, то `libmysqlclient` і потоки по-різному обробляли б значення `MYSQL_OPT_READ_TIMEOUT`