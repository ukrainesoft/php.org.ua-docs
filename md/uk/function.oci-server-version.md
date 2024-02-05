---
navigation:
  - function.oci-rollback.md: « oci\_rollback
  - function.oci-set-action.md: oci\_set\_action »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_server\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_server\_version

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_server\_version — Повертає версію сервера Oracle

### Опис

```methodsynopsis
oci_server_version(resource $connection): string|false
```

Повертає рядок з інформацією про версію сервера Oracle та доступні опції

### Список параметрів

`connection`

### Значення, що повертаються

Повертає у вигляді рядка інформацію про версію або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** oci\_server\_version()\*\*\*\*

```php
<?php

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
echo "Версия сервера: " . oci_server_version($conn);

// Выведет:
// Версия сервера: Oracle Database 11g Enterprise Edition Release 11.2.0.1.0 - 64bit Production
// With the Partitioning, OLAP, Data Mining and Real Application Testing option

oci_close($conn);

?>
```

### Дивіться також

-   [oci\_client\_version()](function.oci-client-version.md) \- Повертає версію клієнтської бібліотеки
