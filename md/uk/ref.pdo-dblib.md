---
navigation:
  - pdo.cubrid-schema.md: '« PDO::cubrid\_schema'
  - ref.pdo-dblib.connection.md: PDO\_DBLIB DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції Microsoft SQL Server та Sybase (PDO\_DBLIB)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції Microsoft SQL Server та Sybase (PDO\_DBLIB)

## Вступ

PDO\_DBLIB - драйвер, реализующий[інтерфейс PHP Data Objects (PDO)](intro.pdo.md) для доступу до баз даних Microsoft SQL Server та Sybase за допомогою бібліотеки FreeTDS.

Модуль недоступний для Windows.

У Windows ви повинні використовувати SqlSrv – альтернативний драйвер для MS SQL, доступний на сайті Microsoft: [» http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx](http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx)

Якщо використовувати SqlSrv неможливо, то для з'єднання з Microsoft SQL Server і Sybase, використовуйте драйвер [PDO\_ODBC](ref.pdo-odbc.md), тому що нативний Windows DB-LIB є давнім, потоконебезпечним і не підтримується Microsoft.

## Зміст

-   [PDO\_DBLIB DSN](ref.pdo-dblib.connection.md)— З'єднання з базами даних Microsoft SQL Server та Sybase
