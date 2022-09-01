---
navigation:
  - function.odbc-close-all.html: « odbccloseall
  - function.odbc-columnprivileges.html: odbccolumnprivileges »
  - index.html: PHP Manual
  - ref.uodbc.html: Функции ODBC
title: odbcclose
---
# odbcclose

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcclose — Закриває з'єднання ODBC

### Опис

```methodsynopsis
odbc_close(resource $odbc): void
```

Закриває з'єднання із сервером бази даних.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbcconnect()](function.odbc-connect.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження**
> 
> Ця функція не спрацює, якщо з'єднання є відкритими транзакціями. У цьому випадку з'єднання залишиться відкритим.
