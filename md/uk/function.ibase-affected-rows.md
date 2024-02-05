---
navigation:
  - function.ibase-add-user.md: « ibase\_add\_user
  - function.ibase-backup.md: ibase\_backup »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_affected\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_affected\_rows

(PHP 5, PHP 7 < 7.4.0)

ibase\_affected\_rows — Повертає кількість рядків, на які вплинув попередній запит

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

-   [ibase\_query()](function.ibase-query.md) \- Виконує запит до бази даних InterBase
-   [ibase\_execute()](function.ibase-execute.md) \- Виконує попередньо підготовлений запит
