---
navigation:
  - function.db2-stmt-error.md: « db2\_stmt\_error
  - function.db2-table-privileges.md: db2\_table\_privileges »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_stmt\_errormsg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_stmt\_errormsg

(PECL ibm\_db2 >= 1.0.0)

db2\_stmt\_errormsg — Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу

### Опис

```methodsynopsis
db2_stmt_errormsg(?resource $stmt = null): string
```

Повертає рядок, який містить останнє повідомлення про помилку SQL-виразу.

Якщо ви не передаєте ресурс виразу як аргумент у **db2\_stmt\_errormsg()**, драйвер повертає повідомлення про помилку, пов'язане з останньою спробою повернути ресурс оператора, наприклад, [db2\_prepare()](function.db2-prepare.md) або [db2\_exec()](function.db2-exec.md)

### Список параметрів

`stmt`

Допустимий ресурс вираження.

### Значення, що повертаються

Повертає рядок, що містить повідомлення про помилку та значення SQLCODE останньої помилки, що виникла під час видачі SQL-виразу.

### Дивіться також

-   [db2\_conn\_error()](function.db2-conn-error.md) \- Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення
-   [db2\_conn\_errormsg()](function.db2-conn-errormsg.md) \- Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2\_stmt\_error()](function.db2-stmt-error.md) \- Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором
