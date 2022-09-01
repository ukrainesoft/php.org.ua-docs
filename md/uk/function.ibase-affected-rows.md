---
navigation:
  - function.ibase-add-user.html: « ibaseadduser
  - function.ibase-backup.html: ibasebackup »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseaffectedrows
---
# ibaseaffectedrows

(PHP 5, PHP 7 < 7.4.0)

ibaseaffectedrows — Повертає кількість рядків, на які вплинув попередній запит

### Опис

```methodsynopsis
ibase_affected_rows(resource $link_identifier = ?): int
```

Ця функція повертає кількість рядків, на які вплинув попередній запит (INSERT, UPDATE або DELETE), виконаний із зазначеного контексту транзакції.

### Список параметрів

`link_identifier`

Контекст транзакції. Якщо `link_identifier` є ресурсом з'єднання, використовується його транзакція за умовчанням.

### Значення, що повертаються

Повертає кількість рядків як цілого числа.

### Дивіться також

-   [ibasequery()](function.ibase-query.md) - Виконує запит до бази даних InterBase
-   [ibaseexecute()](function.ibase-execute.md) - Виконує попередньо підготовлений запит
