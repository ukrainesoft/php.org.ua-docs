---
navigation:
  - ref.pdo-odbc.connection.md: « PDO\_ODBC DSN
  - ref.pdo-pgsql.connection.md: PDO\_PGSQL DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції PostgreSQL (PDO\_PGSQL)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції PostgreSQL (PDO\_PGSQL)

## Вступ

PDO\_PGSQL – це драйвер, що реалізує інтерфейс [PHP Data Objects (PDO)](intro.pdo.md) для доступу до баз даних PostgreSQL.

## Типи ресурсів

Цей модуль визначає потоковий ресурс, що повертається [PDO::pgsqlLOBOpen()](pdo.pgsqllobopen.md)

## Установка

Для установки модуля PDO PostgreSQL используйте опцию**\--with-pdo-pgsql\[=DIR\]**, где`[=DIR]` - необов'язкове значення, що вказує на директорію встановлення бази PostgreSQL або шлях до *pg\_config*

```
$ ./configure --with-pdo-pgsql
```

## Обумовлені константи

Наведені нижче константи визначені цим драйвером і будуть доступні лише у випадку, якщо PHP був зібраний за допомогою цього модуля, або модуль був динамічно завантажений під час виконання. Крім того, ці залежні від драйвера константи повинні бути використані лише разом із цим драйвером. Використання атрибутів, специфічних для деякого драйвера з іншим драйвером, може викликати несподівану поведінку. Якщо ваш код виконується з кількома драйверами, можна використовувати функцію [PDO::getAttribute()](pdo.getattribute.md)для получения атрибута\*\*`PDO::ATTR_DRIVER_NAME`\*\*для проверки драйвера.

**`PDO::PGSQL_ATTR_DISABLE_PREPARES`**(int)

Надішліть запит і параметри на сервер разом за один виклик, уникаючи необхідності окремо створювати іменований підготовлений оператор. Якщо запит виконуватиметься лише один раз, це може зменшити затримку, уникаючи непотрібного обходу сервера.

## Загальні зауваження

> **Зауваження** :
> 
> Поля`bytea` повертаються як потоки.

## Зміст

-   [PDO\_PGSQL DSN](ref.pdo-pgsql.connection.md)— З'єднання з базою даних PostgreSQL
-   [PDO::pgsqlCopyFromArray](pdo.pgsqlcopyfromarray.md) \- Копіювати масив PHP в таблицю
-   [PDO::pgsqlCopyFromFile](pdo.pgsqlcopyfromfile.md)— Копіювати дані з файлу до таблиці
-   [PDO::pgsqlCopyToArray](pdo.pgsqlcopytoarray.md)— Вивантажити дані з таблиці до масиву PHP
-   [PDO::pgsqlCopyToFile](pdo.pgsqlcopytofile.md)— Вивантаження таблиці у файл
-   [PDO::pgsqlGetNotify](pdo.pgsqlgetnotify.md)— Отримати асинхронне повідомлення
-   [PDO::pgsqlGetPid](pdo.pgsqlgetpid.md)— Отримує PID сервера
-   [PDO::pgsqlLOBCreate](pdo.pgsqllobcreate.md)— Створити новий великий об'єкт (LOB)
-   [PDO::pgsqlLOBOpen](pdo.pgsqllobopen.md)— Відкриває потік для існуючого великого об'єкту
-   [PDO::pgsqlLOBUnlink](pdo.pgsqllobunlink.md)— Видалити великий об'єкт
