---
navigation:
  - function.odbc-close-all.md: « odbc\_close\_all
  - function.odbc-columnprivileges.md: odbc\_columnprivileges »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_close

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_close — Закриває з'єднання ODBC

### Опис

```methodsynopsis
odbc_close(resource $odbc): void
```

Закриває з'єднання із сервером бази даних.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження** :
> 
> Ця функція не спрацює, якщо з'єднання є відкритими транзакціями. У цьому випадку з'єднання залишиться відкритим.
