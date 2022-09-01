---
navigation:
  - ref.pdo-firebird.connection.html: « PDOFIREBIRD DSN
  - ref.pdo-ibm.connection.html: PDOIBM DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції IBM (PDOIBM)
---
# Функції IBM (PDOIBM)

## Вступ

PDOIBM – це драйвер, що реалізує інтерфейс [PHP Data Objects (PDO)](intro.pdo.md) для надання можливості працювати з базами даних IBM.

## Встановлення

Для складання модуля PDOIBM у вашій системі має бути встановлений DB2 Client версії v9.1 або вище. DB2 Client можна завантажити з сайту [» сайта разработки приложений IBM](http://www.ibm.com/software/data/db2/ad)

> **Зауваження** **Зверніть увагу**
> 
> DB2 Client версії v9.1 та вище підтримує прямий доступ до DB2 для Linux, UNIX та Windows Server v8 та v9.1.
> 
> Також DB2 Client v9.1 підтримує доступ до серверів DB2 UDB для i5 та DB2 UDB для z/OS, використовуючи окремо куплений [» продукт DB2 Connect](http://www.ibm.com/software/data/db2/db2connect)

PDOIBM – це модуль [» PECL](https://pecl.php.net/), так що дотримуйтесь інструкцій [Установка модулей PECL](install.pecl.md) для встановлення цього модуля. Не забудьте вказати команду **configure** розташування заголовних файлів DB2 Client та бібліотек:

```
bash$ ./configure --with-pdo-ibm=/path/to/sqllib[,shared]
```

Команда **configure** за умовчанням буде використовувати змінну оточення `DB2DIR`

## Зміст

-   [PDOIBM DSN](ref.pdo-ibm.connection.html) — З'єднання з базою даних IBM
