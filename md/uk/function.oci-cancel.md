---
navigation:
  - function.oci-bind-by-name.md: « oci\_bind\_by\_name
  - function.oci-client-version.md: oci\_client\_version »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_cancel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_cancel

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_cancel — Закінчує процес читання з курсору

### Опис

```methodsynopsis
oci_cancel(resource $statement): bool
```

Скидає курсор, звільняючи всі пов'язані ресурси та скасовує можливість читати з нього.

### Список параметрів

`statement`

Запит OCI.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
