---
navigation:
  - function.db2-foreign-keys.md: « db2\_foreign\_keys
  - function.db2-free-stmt.md: db2\_free\_stmt »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_free\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_free\_result

(PECL ibm\_db2 >= 1.0.0)

db2\_free\_result — Звільняє ресурси, пов'язані з набором результатів

### Опис

```methodsynopsis
db2_free_result(resource $stmt): bool
```

Звільняє ресурси системи та бази даних, пов'язані з набором результатів. Ці ресурси неявно звільняються після завершення скрипту, але ви можете викликати **db2\_free\_result()**, щоб явно звільнити ресурси набору результатів до завершення сценарію.

### Список параметрів

`stmt`

Допустимий ресурс вираження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [db2\_free\_stmt()](function.db2-free-stmt.md) \- звільняє ресурси, пов'язані із зазначеним ресурсом вираження
