---
navigation:
  - ref.pdo-cubrid.md: « CUBRID (PDO)
  - pdo.cubrid-schema.md: 'PDO::cubrid\_schema »'
  - index.md: PHP Manual
  - ref.pdo-cubrid.md: CUBRID (PDO)
title: PDO\_CUBRID DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_CUBRID DSN

(PECL PDO\_CUBRID >= 8.3.0.0001)

PDO\_CUBRID DSN — З'єднання з базою даних CUBRID

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDO\_CUBRID складається з наступних елементів, розділених крапкою з комою:

Префікс DSN

**`cubrid:`**

`host`

Ім'я хоста, на якому розгорнуто базу даних.

`port`

Порт, де база даних слухає підключення.

`dbname`

Назва бази даних.

### Примітки

> **Зауваження** :
> 
> При з'єднанні з CUBRID ви повинні вказати ім'я користувача та пароль.

### Приклади

**Приклад #1 Приклад PDO\_CUBRID DSN**

Наступний приклад демонструє PDO\_CUBRID DSN для з'єднання з базою CUBRID:

```
cubrid:host=localhost;port=33000;dbname=demodb
```
