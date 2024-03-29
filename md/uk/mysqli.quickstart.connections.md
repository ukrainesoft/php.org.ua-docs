---
navigation:
  - mysqli.quickstart.dual-interface.md: « Процедурний та об'єктно-орієнтований інтерфейс
  - mysqli.quickstart.statements.md: Виконання запитів »
  - index.md: PHP Manual
  - mysqli.quickstart.md: Короткий посібник
title: З'єднання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## З'єднання

Сервер MySQL підтримує різні способи передачі. З'єднання можуть використовувати протоколи TCP/IP, сокети Unix-доменів або іменовані пайпи Windows.

Имя хоста`localhost` має особливе значення. Воно використовується лише в сокетах доменів Unix. Щоб відкрити TCP/IP-з'єднання з локальним хостом, необхідно використовувати `127.0.0.1`вместо имени хоста`localhost`

**Приклад #1 Спеціальне призначення**

```php
<?php

$mysqli = new mysqli("localhost", "user", "password", "database");

echo $mysqli->host_info . "\n";

$mysqli = new mysqli("127.0.0.1", "user", "password", "database", 3306);

echo $mysqli->host_info . "\n";
```

Результат виконання наведеного прикладу:

```
Localhost via UNIX socket
127.0.0.1 via TCP/IP
```

**Умовчання для параметрів з'єднань**

Залежно від функції, що здійснює підключення, якісь параметри не можна задавати. Якщо параметр не заданий, модуль спробує використати значення за промовчанням для цього параметра, яке встановлено в конфігураційному файлі PHP.

**Приклад #2 Завдання значень за замовчуванням**

mysqli.default\_host=192.168.2.27 mysqli.default\_user=root mysqli.default\_pw="" mysqli.default\_port=3306 mysqli.default\_socket=/tmp/mysql.sock

Далі, щоб встановити з'єднання, функція передає параметри клієнтську бібліотеку, якою користується модуль. Якщо бібліотека виявить порожні або відсутні параметри, вона може встановити замість них свої вбудовані значення за промовчанням.

**Вбудовані бібліотечні значення за промовчанням для параметрів з'єднання**

Якщо ім'я хоста не задано або передано порожній рядок, клієнтська бібліотека використовує для підключення до Unix-сокету хоста `localhost`. Якщо сокет не заданий або передано порожній рядок, і при цьому запитане підключення до Unix-сокету, бібліотека спробує підключитися до сокету `/tmp/mysql.sock`

У Windows-системах, якщо як ім'я хоста передається , бібліотека спробує відкрити з'єднання з урахуванням іменованого пайпа. У цьому випадку ім'я сокета буде сприйнято як пайп. Якщо ім'я сокета не задано, то буде використано значення `\\.\pipe\MySQL`

Якщо з'єднання не використовує ні сокет домену Unix, ні іменований пайп Windows, і при цьому не заданий порт для підключення, бібліотека використовує номер порту `3306`

У драйвері [mysqlnd](mysqlnd.overview.md) та клієнтській бібліотеці MySQL (libmysqlclient) закладена та сама логіка визначення умовчань.

**Налаштування з'єднання**

Налаштування з'єднання дозволяють, наприклад, встановити якісь команди, які потрібно виконати відразу після підключення, або віддати розпорядження використовувати певний набір символів. Установки повинні бути задані до підключення до сервера.

Коли потрібно встановити налаштування з'єднання, операція підключення виконується в три етапи: функцією [mysqli\_init()](mysqli.init.md) або [mysqli::\_\_construct()](mysqli.construct.md) створюється дескриптор підключення, потім підключення налаштовується за допомогою функції [mysqli::options()](mysqli.options.md), і нарешті встановлюється мережне з'єднання з сервером за допомогою функції [mysqli::real\_connect()](mysqli.real-connect.md)

**Об'єднання підключень до пулу**

Модуль mysqli підтримує постійні з'єднання з базою даних, які являють собою спеціальний вид об'єднаних з'єднань. За замовчуванням кожне відкрите скриптом з'єднання закривається або самим скриптом під час виконання, або автоматично після завершення роботи скрипта. Постійні з'єднання відрізняються тим, що не закриваються, а поміщаються в пул для повторного використання надалі. Якщо потрібно підключитися до того ж сервера та бази даних, з тим самим ім'ям користувача, паролем, сокетом і портом, то замість створення нового підключення з пулу виймається вже існуюче. Повторне використання з'єднань дозволяє уникнути накладних витрат на створення нових з'єднань.

Кожен PHP процес використовує свій пул підключень mysqli. Залежно від конфігурації веб-сервера, процес PHP може обслуговувати один або кілька запитів. Відповідно, з'єднання з пулу можуть послідовно використовувати кілька скриптів.

**Постійне з'єднання**

Нове підключення створюється, тільки якщо в кулі не знайдеться вільного підключення з тими самими даними хоста, імені користувача, пароля, сокету, порту та бази даних за промовчанням. Механізм постійних з'єднань можна включати та вимикати PHP директивою [mysqli.allow\_persistent](mysqli.configuration.md#ini.mysqli.allow-persistent). Максимальна кількість з'єднань, які може відкрити скрипт, обмежена значенням [mysqli.max\_links](mysqli.configuration.md#ini.mysqli.max-links). Максимальна кількість з'єднань, які може відкрити один PHP-процес, обмежена значенням [mysqli.max\_persistent](mysqli.configuration.md#ini.mysqli.max-persistent). Слід зазначити, що веб-сервер може породжувати безліч процесів PHP.

Головний недолік постійних підключень полягає в тому, що перед повторним використанням їхній стан не скидається до первісного. Наприклад, відкриті та незавершені транзакції не будуть автоматично відкочуватися. Також, якщо під час знаходження з'єднання в пулі для процесу змінилися будь-які дозволи або рівні доступу, цей факт ніяк не вплине на підключення під час його вилучення з пулу. Така поведінка може спричинити небажані результати. Хоча, з іншого боку, назва `постійний` можна розглядати, як обіцянку, що підключення і справді залишиться в тому стані, в якому воно було поміщене в пул.

Модуль mysqli підтримує обидві інтерпретації терміну постійне з'єднання: стан з'єднання може зберігатися, а може скидатися в початкове. За замовчуванням під час вилучення з пулу з'єднання скидається. mysqli робить це неявним викликом функції [mysqli::change\_user()](mysqli.change-user.md) щоразу, коли підключення використовується повторно. З точки зору користувача підключення виглядає, як щойно створене.

Однак, виклик функції [mysqli::change\_user()](mysqli.change-user.md) Досить дорога операція. Для покращення швидкодії можна перекомпілювати модуль із встановленим прапором **`MYSQLI_NO_CHANGE_USER_ON_PCONNECT`**

Вибір між безпечною поведінкою підключень та найкращою швидкодією залишається за користувачем. Тут не можна дати однозначної поради. Для простоти використання, за умовчанням увімкнено безпечний режим з очищенням з'єднань.

**Дивіться також**

-   [mysqli::\_\_construct()](mysqli.construct.md)
-   [mysqli\_init()](mysqli.init.md)
-   [mysqli::options()](mysqli.options.md)
-   [mysqli::real\_connect()](mysqli.real-connect.md)
-   [mysqli::change\_user()](mysqli.change-user.md)
-   [$mysqli::host\_info](mysqli.get-host-info.md)
-   [MySQLi Configuration Options](mysqli.configuration.md)
-   [Persistent Database Connections](features.persistent-connections.md)
