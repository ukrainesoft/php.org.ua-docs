---
navigation:
  - mysqli.requirements.md: « Вимоги
  - mysqli.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - mysqli.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Модуль`mysqli` був представлений із версією PHP 5.0.0. MySQL Native Driver був включений до PHP версії 5.3.0.

## Установка для Linux

Більшість дистрибутивів Unix включає бінарні версії PHP, які надалі можуть бути встановлені. Незважаючи на те, що бінарні версії, як правило, зібрані з увімкненою підтримкою модулів MySQL, може знадобитися встановлення додаткових пакетів з бібліотеками модулів. Переконайтеся, що менеджер пакетів, що йде з вибраним дистрибутивом, дозволяє встановити такі пакети.

К Прикладу, на Ubuntu пакет`php5-mysql` встановлює модулі ext/mysql, ext/mysqli та pdo\_mysql. В CentOS пакет`php-mysql` також встановлює три ці модулі.

Звичайно, ви завжди можете зібрати PHP із вихідного коду. Складання PHP з вихідного коду дозволяє виділити тільки ті модулі MySQL (а також клієнтські бібліотеки для кожного з модулів), які потрібно використовувати.

Рекомендується використовувати бібліотеку MySQL Native Driver, оскільки вона підвищує продуктивність та дає доступ до функцій, недоступних під час використання MySQL Client Library. Дивіться [Що таке MySQL Native Driver у PHP?](mysqli.overview.md#mysqli.overview.mysqlnd) для ознайомлення із можливостями MySQL Native Driver.

Под`/path/to/mysql_config` мається на увазі розташування програми `mysql_config`, що постачається разом з MySQL Server.

**Допоміжна таблиця часу компіляції mysqli**

| Версия PHP | По умолчанию | Опции настройки: [mysqlnd](mysqlnd.overview.md) | Опции настройки: `libmysqlclient` | Список изменений |
| --- | --- | --- | --- | --- |
| 5.4.x і вище | mysqlnd | **\--with-mysqli** | **\--with-mysqli=/path/to/mysql\_config** | за замовчуванням mysqlnd |
| 5.3.x | libmysqlclient | **\--with-mysqli=mysqlnd** | **\--with-mysqli=/path/to/mysql\_config** | mysqlnd підтримується |
| 5.0.x, 5.1.x, 5.2.x | libmysqlclient | Недоступно | **\--with-mysqli=/path/to/mysql\_config** | mysqlnd не підтримується |

Існує можливість вільно перемішувати модулі MySQL і клієнтські бібліотеки. Наприклад, можна активувати модуль MySQL, що дозволяє використовувати MySQL Client Library (libmysqlclient), і при цьому налаштувати модуль `mysqli` для використання MySQL Native Driver. Таким чином, можливі будь-які перестановки модулів та клієнтських бібліотек.

## Установка для Windows

У Windows DLL php\_mysqli.dll повинен бути включений до php.ini.

Як і при включенні будь-якого модуля PHP (наприклад, php\_mysqli.dll), директива PHP[extension\_dir](ini.core.md#ini.extension-dir) повинна встановлювати каталог, у якому перебувають модулі PHP. Дивіться також розділ про [самостійної установки PHP у Windows](install.windows.manual.md)Приклад значения`extension_dir`\- c:\\php\\ext.

> **Зауваження** :
> 
> Якщо під час запуску веб-сервера виникає помилка, подібна до наступної: `"Unable to load dynamic library './php_mysqli.dll'"`це відбувається тому, що файл php\_mysqli.dll не може бути знайдено системою.
