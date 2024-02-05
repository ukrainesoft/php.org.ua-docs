---
navigation:
  - function.db2-connect.md: « db2\_connect
  - function.db2-escape-string.md: db2\_escape\_string »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_cursor\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_cursor\_type

(PECL ibm\_db2 >= 1.0.0)

db2\_cursor\_type — Повертає тип курсору, який використовується у ресурсі оператора

### Опис

```methodsynopsis
db2_cursor_type(resource $stmt): int
```

Повертає тип курсору, який використовується у ресурсі оператора.

### Список параметрів

`stmt`

Коректний ресурс оператора.

### Значення, що повертаються

Повертає або `DB2_FORWARD_ONLY`, либо`DB2_SCROLLABLE`, в залежності від типу курсора, що використовується.

### Дивіться також

-   [db2\_prepare()](function.db2-prepare.md) \- готує SQL-запит до виконання
