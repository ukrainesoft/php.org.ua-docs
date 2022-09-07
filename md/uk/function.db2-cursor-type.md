---
navigation:
  - function.db2-connect.md: « db2connect
  - function.db2-escape-string.md: db2escapestring »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2cursortype
---
# db2cursortype

(PECL ibmdb2> = 1.0.0)

db2cursortype — Повертає тип курсору, який використовується у ресурсі оператора

### Опис

```methodsynopsis
db2_cursor_type(resource $stmt): int
```

Повертає тип курсору, який використовується у ресурсі оператора.

### Список параметрів

`stmt`

Коректний ресурс оператора.

### Значення, що повертаються

Повертає або `DB2_FORWARD_ONLY`, або `DB2_SCROLLABLE`, в залежності від типу курсора, що використовується.

### Дивіться також

-   [db2prepare()](function.db2-prepare.md) - готує SQL-запит до виконання
