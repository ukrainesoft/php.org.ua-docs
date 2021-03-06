- [« Вимоги](mysqli.requirements.md)
- [Налаштування під час виконання »](mysqli.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](mysqli.setup.md)
- Встановлення

## Установка

Модуль `mysqli` був представлений із версією PHP 5.0.0. MySQL Native Driver
був включений до PHP версії 5.3.0.

## Установка для Linux

Більшість дистрибутивів Unix включає бінарні версії PHP, які в
надалі можуть бути встановлені. Незважаючи на те, що бінарні версії,
як правило, зібрані з включеною підтримкою модулів MySQL, може
потрібно встановити додаткові пакети з бібліотеками модулів.
Переконайтеся, що менеджер пакетів, що йде з вибраним дистрибутивом,
дозволяє встановити такі пакети.

Наприклад, на Ubuntu пакет `php5-mysql` встановлює модулі ext/mysql,
ext/mysqli, та pdo_mysql. У CentOS пакет `php-mysql` також встановлює
три ці модулі.

Звичайно, ви завжди можете зібрати PHP із вихідного коду. Складання PHP з
вихідного коду дозволяє виділити тільки ті модулі MySQL (а також
клієнтські бібліотеки для кожного з модулів), які потрібні
використовувати.

Рекомендується використовувати бібліотеку MySQL Native Driver, оскільки вона
підвищує продуктивність і дає доступ до функцій, недоступних при
використання MySQL Client Library. Дивіться [Що таке MySQL Native Driver в PHP?](mysqli.overview.md#mysqli.overview.mysqlnd) для
ознайомлення із можливостями MySQL Native Driver.

Під `/path/to/mysql_config` мається на увазі розташування програми
`mysql_config`, що поставляється разом з MySQL Server.

| Версія PHP За замовчуванням | Опції налаштування: [mysqlnd](mysqlnd.overview.md) | Опції налаштування: libmysqlclient | Список змін                             |
| --------------------------- | -------------------------------------------------- | ---------------------------------- | --------------------------------------- |
| 5.4.x та вище               | mysqlnd                                            | **--with-mysqli**                  | **--with-mysqli=/path/to/mysql_config** | за промовчанням mysqlnd
| 5.3.x                       | libmysqlclient                                     | **--with-mysqli=mysqlnd**          | **--with-mysqli=/path/to/mysql_config** | mysqlnd підтримується
| 5.0.x, 5.1.x, 5.2.x         | libmysqlclient                                     | Недоступний                        | **--with-mysqli=/path/to/mysql_config** | mysqlnd не підтримується

**Допоміжна таблиця часу компіляції mysqli**

Слід зазначити, що є можливість вільно перемішувати
модулі MySQL та клієнтські бібліотеки. Наприклад, можна активувати
модуль MySQL, який дозволяє використовувати MySQL Client Library
(libmysqlclient), і при цьому налаштувати модуль `mysqli` для використання
MySQL Native Driver. Таким чином, можливі будь-які перестановки модулів
та клієнтських бібліотек.

## Установка для Windows

Для Windows PHP в більшості випадків встановлюється за допомогою
установника.

## PHP 5.3.0 та новіший

У Windows для PHP версії 5.3 і вище, модуль mysqli включений і
використовує MySQL Native Driver за промовчанням. Це означає, що вам не
потрібно турбуватися про налаштування доступу до `libmysql.dll`.

## PHP 5.0, 5.1, 5.2

Для старих, непідтримуваних версій PHP (PHP 5.2 не підтримується з 6
січня 2011 року), необхідно зробити налаштування для включення модуля
`mysqli` та визначення використовуваної ним клієнтської бібліотеки.

Модуль `mysqli` не включений за замовчуванням, тому в `php.ini` необхідно
вказати файл DLL `php_mysqli.dll`. Для цього вам потрібно знайти файл
`php.ini` (зазвичай розташований у `c:\php`) і переконатися, що ви зняли знак
коментування (";") на початку рядка `extension=php_mysqli.dll`, в
розділ `[PHP_MYSQLI]`.

Також, якщо ви хочете використовувати MySQL Client Library з `mysqli`, то
Вам необхідно переконатися, що PHP може отримати доступ до файлу
клієнтської бібліотеки. MySQL Client Library включений до дистрибутиву
Windows PHP у вигляді файлу `libmysql.dll`. Цей файл має бути доступним
у змінному оточенні Windows `PATH` для того, щоб його можна було
успішно завантажити. За посиланням "[Як додати мою PHP директорію в Windows PATH](faq.installation.md#faq.installation.addtopath)"
міститься стаття з інформацією про те, як це зробити. Якщо системна
директорія Windows прописана в `PATH`, то можна скопіювати
`libmysql.dll` в системну директорію Windows (зазвичай
`c:\Windows\system`). Однак такий шлях не рекомендується.

При включенні будь-якого модуля PHP (наприклад, `php_mysqli.dll`), директива
PHP [extension_dir](ini.core.md#ini.extension-dir) має містити
шлях до директорії, де є модулі PHP. Дивіться також [Інструкції самостійної установки для Windows](install.windows.manual.md).
Наприклад, у PHP 5 значенням `extension_dir` є `c:\php xt`.

> **Примітка**:
>
> Якщо під час завантаження сервера з'являється таке повідомлення:
> ``Unable to load dynamic library './php_mysqli.dll''`, то система не
> може знайти файли `php_mysqli.dll` та/або `libmysql.dll`.
