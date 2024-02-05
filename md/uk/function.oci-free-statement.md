---
navigation:
  - function.oci-free-descriptor.md: « oci\_free\_descriptor
  - function.oci-get-implicit-resultset.md: oci\_get\_implicit\_resultset »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_free\_statement
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_free\_statement

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_free\_statement — Звільняє ресурси, які займає курсор або SQL-вираз.

### Опис

```methodsynopsis
oci_free_statement(resource $statement): bool
```

Звільняє всі ресурси, що займаються курсором або SQL-виразом, яке повернуто функцією [oci\_parse()](function.oci-parse.md)или получено от сервера Oracle.

### Список параметрів

`statement`

Допустимий ідентифікатор OCI-виразу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
