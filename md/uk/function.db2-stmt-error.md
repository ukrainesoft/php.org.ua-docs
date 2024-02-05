---
navigation:
  - function.db2-statistics.md: « db2\_statistics
  - function.db2-stmt-errormsg.md: db2\_stmt\_errormsg »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_stmt\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_stmt\_error

(PECL ibm\_db2 >= 1.0.0)

db2\_stmt\_error — Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором

### Опис

```methodsynopsis
db2_stmt_error(?resource $stmt = null): string
```

Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором.

Якщо ви не передасте ресурс оператора як аргумент у **db2\_stmt\_error()**, драйвер поверне значення SQLSTATE, пов'язане з останньою спробою повернути ресурс оператора, наприклад, з [db2\_prepare()](function.db2-prepare.md) або [db2\_exec()](function.db2-exec.md)

Щоб дізнатися, що означає SQLSTATE, можна ввести наступну команду в командному рядку процесора DB2: **``db2 '? `sqlstate-value`'``**. Ви також можете викликати [db2\_stmt\_errormsg()](function.db2-stmt-errormsg.md), щоб отримати явне повідомлення про помилку та відповідне значення SQLCODE.

### Список параметрів

`stmt`

Допустимий ресурс оператора.

### Значення, що повертаються

Повертає рядок, який містить значення SQLSTATE.

### Дивіться також

-   [db2\_conn\_error()](function.db2-conn-error.md) \- Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення
-   [db2\_conn\_errormsg()](function.db2-conn-errormsg.md) \- Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2\_stmt\_errormsg()](function.db2-stmt-errormsg.md) \- Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу
