---
navigation:
  - function.odbc-binmode.md: « odbc\_binmode
  - function.odbc-close.md: odbc\_close »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_close\_all
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_close\_all

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_close\_all — Закриває всі з'єднання ODBC

### Опис

```methodsynopsis
odbc_close_all(): void
```

**odbc\_close\_all()** закриє всі з'єднання із сервером (серверами) бази даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження** :
> 
> Ця функція не спрацює, якщо з'єднання є відкритими транзакціями. У цьому випадку з'єднання залишиться відкритим.
