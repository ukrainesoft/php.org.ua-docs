---
navigation:
  - function.db2-stmt-error.md: « db2stmterror
  - function.db2-table-privileges.md: db2tableprivileges »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2stmterrormsg
---
# db2stmterrormsg

(PECL ibmdb2> = 1.0.0)

db2stmterrormsg — Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу

### Опис

```methodsynopsis
db2_stmt_errormsg(resource $stmt = ?): string
```

Повертає рядок, який містить останнє повідомлення про помилку SQL-виразу.

Якщо ви не передаєте ресурс виразу як аргумент у **db2stmterrormsg()**, драйвер повертає повідомлення про помилку, пов'язане з останньою спробою повернути ресурс оператора, наприклад, [db2prepare()](function.db2-prepare.md) або [db2exec()](function.db2-exec.md)

### Список параметрів

`stmt`

Допустимий ресурс вираження.

### Значення, що повертаються

Повертає рядок, що містить повідомлення про помилку та значення SQLCODE останньої помилки, що виникла під час видачі SQL-виразу.

### Дивіться також

-   [db2connerror()](function.db2-conn-error.md) - Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення
-   [db2connerrormsg()](function.db2-conn-errormsg.md) - Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2stmterror()](function.db2-stmt-error.md) - Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором
