---
navigation:
  - function.oci-rollback.md: « ocirollback
  - function.oci-set-action.md: ocisetaction »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ociserverversion
---
# ociserverversion

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ociserverversion — Повертає версію сервера Oracle

### Опис

```methodsynopsis
oci_server_version(resource $connection): string|false
```

Повертає рядок з інформацією про версію сервера Oracle та доступні опції

### Список параметрів

`connection`

### Значення, що повертаються

Повертає у вигляді рядка інформацію про версію або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ociserverversion()****

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

### Примітки

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ociserverversion()](function.ociserverversion.md). У PHP 5.0.0 і вище [ociserverversion()](function.ociserverversion.md) є аліасом \*\*ociserverversion()\*\*Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.

### Дивіться також

-   [ociclientversion()](function.oci-client-version.md) - Повертає версію клієнтської бібліотеки
