Отримує попередження від останньої операції

-   [« SqlStatementResult::getLastInsertId](mysql-xdevapi-sqlstatementresult.getlastinsertid.html)
    
-   [SqlStatementResult::getWarningsCount »](mysql-xdevapi-sqlstatementresult.getwarningcount.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSqlStatementResult](class.mysql-xdevapi-sqlstatementresult.html)
    
-   Отримує попередження від останньої операції
    

# SqlStatementResult::getWarnings

(No version information available, might only be in Git)

SqlStatementResult::getWarnings — Отримує попередження від останньої операції

### Опис

```methodsynopsis
public mysql_xdevapi\SqlStatementResult::getWarnings(): array
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів Warning із останньої операції. Кожен об'єкт визначає 'message' про помилку, 'level' помилки та 'code' помилки. Порожній масив повертається, якщо помилок немає.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSqlStatementResult::getWarnings()****

```php
<?php

/* ... */

?>
```