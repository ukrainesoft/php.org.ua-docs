---
navigation:
  - function.odbc-binmode.md: « odbcbinmode
  - function.odbc-close.md: odbcclose »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbccloseall
---
# odbccloseall

(PHP 4, PHP 5, PHP 7, PHP 8)

odbccloseall — Закриває всі з'єднання ODBC

### Опис

```methodsynopsis
odbc_close_all(): void
```

**odbccloseall()** закриє всі з'єднання із сервером (серверами) бази даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження**
> 
> Ця функція не спрацює, якщо з'єднання є відкритими транзакціями. У цьому випадку з'єднання залишиться відкритим.
