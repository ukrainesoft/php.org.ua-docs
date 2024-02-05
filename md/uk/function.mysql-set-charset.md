---
navigation:
  - function.mysql-select-db.md: « mysql\_select\_db
  - function.mysql-stat.md: mysql\_stat »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_set\_charset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_set\_charset

(PHP 5 >= 5.2.3)

mysql\_set\_charset — Встановлює кодування клієнта

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_set\_charset()](mysqli.set-charset.md)
-   PDO: Додаванням`charset`у рядок з'єднання, наприклад`charset=utf8`

### Опис

```methodsynopsis
mysql_set_charset(string $charset, resource $link_identifier = NULL): bool
```

Встановлює стандартне кодування для поточного з'єднання.

### Список параметрів

`charset`

Коректна назва кодування.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Ця функція вимагає версії MySQL 5.0.7 або вище.

> **Зауваження** :
> 
> Це найбільш вподобаний спосіб зміни кодування. Використання [mysql\_query()](function.mysql-query.md) з цією метою (наприклад `SET NAMES utf8`) не рекомендуется. Смотрите раздел[кодування символів у MySQL](mysqlinfo.concepts.charset.md) для детальної інформації.

### Дивіться також

-   [Налаштування коду символів у MySQL](mysqlinfo.concepts.charset.md)
-   [» Список підтримуваних MySQL кодувань](http://dev.mysql.com/doc/mysql/en/charset-charsets.md)
-   [mysql\_client\_encoding()](function.mysql-client-encoding.md) \- Повертає кодування з'єднання
