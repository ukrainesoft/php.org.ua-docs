---
navigation:
  - mysql-xdevapi-sqlstatementresult.getlastinsertid.md: '« SqlStatementResult::getLastInsertId'
  - mysql-xdevapi-sqlstatementresult.getwarningcount.md: 'SqlStatementResult::getWarningsCount »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-sqlstatementresult.md: mysql\_xdevapi\\SqlStatementResult
title: 'SqlStatementResult::getWarnings'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SqlStatementResult::getWarnings

(No version information available, might only be in Git)

SqlStatementResult::getWarnings — Отримує попередження від останньої операції

### Опис

```methodsynopsis
public mysql_xdevapi\SqlStatementResult::getWarnings(): array
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів Warning із останньої операції. Кожен об'єкт визначає 'message' про помилку, 'level' помилки та 'code' помилки. Порожній масив повертається, якщо помилок немає.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\SqlStatementResult::getWarnings()\*\*\*\*

```php
<?php

/* ... */

?>
```
