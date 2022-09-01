---
navigation:
  - class.mysqli-sql-exception.html: « mysqlisqlexception
  - ref.mysqli.md: Синоніми та застарілі функції Mysqli »
  - index.md: PHP Manual
  - class.mysqli-sql-exception.html: mysqlisqlexception
title: 'mysqlisqlexception::getSqlState'
---
# mysqlisqlexception::getSqlState

(PHP 8> = 8.1.2)

mysqlisqlexception::getSqlState — Повертає код помилки SQLSTATE

### Опис

```methodsynopsis
public mysqli_sql_exception::getSqlState(): string
```

Повертає рядок, який містить код останньої помилки SQLSTATE. Код помилки складається із п'яти символів. Значення задаються ANSI SQL та ODBC. Список можливих значень можна переглянути на сторінці [» http://dev.mysql.com/doc/mysql/en/error-handling.html](http://dev.mysql.com/doc/mysql/en/error-handling.html)

> **Зауваження**
> 
> Зауважте, що не всі помилки MySQL ще зіставлені з SQLSTATE. Якщо помилка не зіставлена, використовується значення `HY000` (Загальна помилка).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, який містить код останньої помилки SQLSTATE. Код помилки складається із п'яти символів.
