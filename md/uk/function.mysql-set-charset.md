---
navigation:
  - function.mysql-select-db.md: « mysqlselectдб
  - function.mysql-stat.md: mysqlstat »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlsetcharset
---
# mysqlsetcharset

(PHP 5> = 5.2.3)

mysqlsetcharset — Встановлює кодування клієнта

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlisetcharset()](mysqli.set-charset.md)
-   PDO: Додаванням `charset` у рядок з'єднання, наприклад `charset=utf8`

### Опис

```methodsynopsis
mysql_set_charset(string $charset, resource $link_identifier = NULL): bool
```

Встановлює стандартне кодування для поточного з'єднання.

### Список параметрів

`charset`

Коректна назва кодування.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Ця функція вимагає версії MySQL 5.0.7 або вище.

> **Зауваження**
> 
> Це найбільш вподобаний спосіб зміни кодування. Використання [mysqlquery()](function.mysql-query.md) з цією метою (наприклад `SET NAMES utf8`) не рекомендується. Дивіться розділ [кодування символів у MySQL](mysqlinfo.concepts.charset.md) для детальної інформації.

### Дивіться також

-   [Налаштування коду символів у MySQL](mysqlinfo.concepts.charset.md)
-   [» Список підтримуваних MySQL кодувань](http://dev.mysql.com/doc/mysql/en/charset-charsets.md)
-   [mysqlclientencoding()](function.mysql-client-encoding.md) - Повертає кодування з'єднання
