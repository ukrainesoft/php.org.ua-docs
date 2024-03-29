---
navigation:
  - function.mysql-get-server-info.md: « mysql\_get\_server\_info
  - function.mysql-insert-id.md: mysql\_insert\_id »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_info

(PHP 4 >= 4.3.0, PHP 5)

mysql\_info — Повертає інформацію про останній запит

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_info()](mysqli.info.md)

### Опис

```methodsynopsis
mysql_info(resource $link_identifier = NULL): string
```

Повертає докладну інформацію про останній запит.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає інформацію про запит у разі успішного виконання, або **`false`** у разі виникнення помилки. Дивіться приклад нижче для яких запитів повертається інформація і як виглядають значення, що повертаються. Для не перерахованих запитів буде повернено значення **`false`**

### Приклади

**Приклад #1 Коректні види запитів MySQL**

Числа розставлені лише для прикладу - їх значення залежить від результату запиту.

INSERT INTO ... SELECT ... String format: Records: 23 Duplicates: 0 Warnings: 0 INSERT INTO ... VALUES (...),(...),(...)... String format: Records: 37 Duplicates: 0 Warnings: 0 LOAD DATA INFILE ... String format: Records: 42 Deleted: 0 Skipped: 0 Warnings: 0 ALTER TABLE String format: Records: 60 Duplicates: 0 Warnings: 0 UPDATE String format: Rows matched: 65 Changed: 65 Warnings: 0

### Примітки

> **Зауваження** :
> 
> **mysql\_info()** повертає значення не рівне **`false`** для INSERT ... VALUES тільки в тому випадку, якщо у запиті є кілька списків значень.

### Дивіться також

-   [mysql\_affected\_rows()](function.mysql-affected-rows.md) \- Повертає кількість порушених минулою операцією рядів
-   [mysql\_insert\_id()](function.mysql-insert-id.md) \- Повертає ідентифікатор, згенерований при останньому INSERT-запиті
-   [mysql\_stat()](function.mysql-stat.md) \- Повертає поточний статус сервера
