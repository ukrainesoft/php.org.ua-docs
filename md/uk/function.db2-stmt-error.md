Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором

-   [« db2\_statistics](function.db2-statistics.html)
    
-   [db2\_stmt\_errormsg »](function.db2-stmt-errormsg.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IBM DB2](ref.ibm-db2.html)
    
-   Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором
    

# db2stmterror

(PECL ibmdb2> = 1.0.0)

db2stmterror — Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором

### Опис

```methodsynopsis
db2_stmt_error(resource $stmt = ?): string
```

Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором.

Якщо ви не передасте ресурс оператора як аргумент у **db2stmterror()**, драйвер поверне значення SQLSTATE, пов'язане з останньою спробою повернути ресурс оператора, наприклад, з [db2\_prepare()](function.db2-prepare.html) або [db2\_exec()](function.db2-exec.html)

Щоб дізнатися, що означає SQLSTATE, можна ввести наступну команду в командному рядку процесора DB2: **``db2 '? `sqlstate-value`'``**. Ви також можете викликати [db2\_stmt\_errormsg()](function.db2-stmt-errormsg.html), щоб отримати явне повідомлення про помилку та відповідне значення SQLCODE.

### Список параметрів

`stmt`

Допустимий ресурс оператора.

### Значення, що повертаються

Повертає рядок, який містить значення SQLSTATE.

### Дивіться також

-   [db2\_conn\_error()](function.db2-conn-error.html) - Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення
-   [db2\_conn\_errormsg()](function.db2-conn-errormsg.html) - Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2\_stmt\_errormsg()](function.db2-stmt-errormsg.html) - Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу