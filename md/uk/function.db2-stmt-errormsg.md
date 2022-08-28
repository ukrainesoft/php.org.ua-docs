Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу

-   [« db2\_stmt\_error](function.db2-stmt-error.html)
    
-   [db2\_table\_privileges »](function.db2-table-privileges.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IBM DB2](ref.ibm-db2.html)
    
-   Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу
    

# db2stmterrormsg

(PECL ibmdb2> = 1.0.0)

db2stmterrormsg — Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу

### Опис

```methodsynopsis
db2_stmt_errormsg(resource $stmt = ?): string
```

Повертає рядок, який містить останнє повідомлення про помилку SQL-виразу.

Якщо ви не передаєте ресурс виразу як аргумент у **db2stmterrormsg()**, драйвер повертає повідомлення про помилку, пов'язане з останньою спробою повернути ресурс оператора, наприклад, [db2\_prepare()](function.db2-prepare.html) або [db2\_exec()](function.db2-exec.html)

### Список параметрів

`stmt`

Допустимий ресурс вираження.

### Значення, що повертаються

Повертає рядок, що містить повідомлення про помилку та значення SQLCODE останньої помилки, що виникла під час видачі SQL-виразу.

### Дивіться також

-   [db2\_conn\_error()](function.db2-conn-error.html) - Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення
-   [db2\_conn\_errormsg()](function.db2-conn-errormsg.html) - Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2\_stmt\_error()](function.db2-stmt-error.html) - Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором