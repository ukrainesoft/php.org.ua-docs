---
navigation:
  - function.db2-free-result.md: « db2\_free\_result
  - function.db2-get-option.md: db2\_get\_option »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_free\_stmt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_free\_stmt

(PECL ibm\_db2 >= 1.0.0)

db2\_free\_stmt - Звільняє ресурси, пов'язані із зазначеним ресурсом виразу

### Опис

```methodsynopsis
db2_free_stmt(resource $stmt): bool
```

Звільняє ресурси системи та бази даних, пов'язані з ресурсом вираження. Ці ресурси неявно звільняються після завершення скрипту, але ви можете викликати **db2\_free\_stmt()**, щоб явно звільнити вирази до закінчення роботи скрипта.

### Список параметрів

`stmt`

Допустимий ресурс вираження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [db2\_free\_result()](function.db2-free-result.md) \- звільняє ресурси, пов'язані з набором результатів
