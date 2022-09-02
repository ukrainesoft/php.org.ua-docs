---
navigation:
  - pdo.cubrid-schema.md: '« PDO::cubridschema'
  - ref.pdo-dblib.connection.md: PDODBLIB DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції Microsoft SQL Server та Sybase (PDODBLIB)
---
# Функції Microsoft SQL Server та Sybase (PDODBLIB)

## Вступ

PDODBLIB – драйвер, що реалізує [интерфейс PHP Data Objects (PDO)](intro.pdo.md) для доступу до баз даних Microsoft SQL Server та Sybase за допомогою бібліотеки FreeTDS.

Модуль недоступний для Windows.

У Windows ви повинні використовувати SqlSrv – альтернативний драйвер для MS SQL, доступний на сайті Microsoft: [» http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx](http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx)

Якщо використовувати SqlSrv неможливо, то для з'єднання з Microsoft SQL Server і Sybase, використовуйте драйвер [PDOODBC](ref.pdo-odbc.md), тому що нативний Windows DB-LIB є давнім, потоконебезпечним і не підтримується Microsoft.

## Зміст

-   [PDODBLIB DSN](ref.pdo-dblib.connection.md) — З'єднання з базами даних Microsoft SQL Server та Sybase
