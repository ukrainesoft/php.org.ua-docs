---
navigation:
  - odbc.installation.md: « Установка
  - uodbc.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - uodbc.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Установки конфігурації Unified ODBC**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [odbc.defaultдб](odbc.configuration.html#ini.uodbc.default-db) | NULL | PHPINIALL |  |
| [odbc.defaultuser](odbc.configuration.html#ini.uodbc.default-user) | NULL | PHPINIALL |  |
| [odbc.defaultпв](odbc.configuration.html#ini.uodbc.default-pw) | NULL | PHPINIALL |  |
| [odbc.allowpersistent](odbc.configuration.html#ini.uodbc.allow-persistent) | "1" | PHPINISYSTEM |  |
| [odbc.checkpersistent](odbc.configuration.html#ini.uodbc.check-persistent) | "1" | PHPINISYSTEM |  |
| [odbc.maxpersistent](odbc.configuration.html#ini.uodbc.max-persistent) | "-1" | PHPINISYSTEM |  |
| [odbc.maxlinks](odbc.configuration.html#ini.uodbc.max-links) | "-1" | PHPINISYSTEM |  |
| [odbc.defaultlrl](odbc.configuration.html#ini.uodbc.defaultlrl) | "4096" | PHPINIALL |  |
| [odbc.defaultbinmode](odbc.configuration.html#ini.uodbc.defaultbinmode) | "1" | PHPINIALL |  |
| [odbc.defaultcursortype](odbc.configuration.html#ini.uodbc.defaultcursortype) | "3" | PHPINIALL |  |

> **Зауваження**: Записи, позначені ще не реалізовані.

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`odbc.default_db` string

Джерело даних ODBC для використання, якщо жоден не вказаний у [odbcconnect()](function.odbc-connect.html) або [odbcpconnect()](function.odbc-pconnect.html)

`odbc.default_user` string

Ім'я користувача для використання, якщо жоден не вказано [odbcconnect()](function.odbc-connect.html) або [odbcpconnect()](function.odbc-pconnect.html)

`odbc.default_pw` string

Пароль для використання, якщо жоден не вказано в [odbcconnect()](function.odbc-connect.html) або [odbcpconnect()](function.odbc-pconnect.html)

`odbc.allow_persistent` bool

Чи дозволяти постійні з'єднання ODBC.

`odbc.check_persistent` bool

Перед повторним використанням переконайтеся, що з'єднання все ще доступне.

`odbc.max_persistent` int

Максимальна кількість постійних з'єднань ODBC на процес.

`odbc.max_links` int

Максимальна кількість з'єднань ODBC на процес, включаючи постійні з'єднання.

`odbc.defaultlrl` int

Обробка довгих (LONG) полів. Визначає кількість байтів, що повертаються змінним. Дивіться [odbclongreadlen()](function.odbc-longreadlen.html) для подробиць.

Якщо використовується int значення вимірюється байтами. Ви також можете використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.html#faq.using.shorthandbytes)

`odbc.defaultbinmode` int

Обробка двійкових даних. Дивіться [odbcbinmode()](function.odbc-binmode.html) для подробиць.

`odbc.default_cursortype` int

Керує моделлю курсору ODBC. Можливі значення **`SQL_CURSOR_FORWARD_ONLY`** **`SQL_CURSOR_KEYSET_DRIVEN`** **`SQL_CURSOR_DYNAMIC`** і **`SQL_CURSOR_STATIC`** (за замовчуванням).
