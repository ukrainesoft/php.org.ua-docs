---
navigation:
  - function.db2-statistics.html: « db2statistics
  - function.db2-stmt-errormsg.html: db2stmterrormsg »
  - index.html: PHP Manual
  - ref.ibm-db2.html: Функції IBM DB2
title: db2stmterror
---
# db2stmterror

(PECL ibmdb2> = 1.0.0)

db2stmterror — Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором

### Опис

```methodsynopsis
db2_stmt_error(resource $stmt = ?): string
```

Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором.

Якщо ви не передасте ресурс оператора як аргумент у **db2stmterror()**, драйвер поверне значення SQLSTATE, пов'язане з останньою спробою повернути ресурс оператора, наприклад, з [db2prepare()](function.db2-prepare.html) або [db2exec()](function.db2-exec.html)

Щоб дізнатися, що означає SQLSTATE, можна ввести наступну команду в командному рядку процесора DB2: **``db2 '? `sqlstate-value`'``**. Ви також можете викликати [db2stmterrormsg()](function.db2-stmt-errormsg.html), щоб отримати явне повідомлення про помилку та відповідне значення SQLCODE.

### Список параметрів

`stmt`

Допустимий ресурс оператора.

### Значення, що повертаються

Повертає рядок, який містить значення SQLSTATE.

### Дивіться також

-   [db2connerror()](function.db2-conn-error.html) - Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення
-   [db2connerrormsg()](function.db2-conn-errormsg.html) - Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2stmterrormsg()](function.db2-stmt-errormsg.html) - Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу
