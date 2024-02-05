---
navigation:
  - function.apache-child-terminate.md: « apache\_child\_terminate
  - function.apache-get-version.md: apache\_get\_version »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_get\_modules
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_get\_modules

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

apache\_get\_modules — Повертає список завантажених модулів сервера Apache

### Опис

```methodsynopsis
apache_get_modules(): array
```

Повертає список завантажених модулів сервера Apache.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) завантажених модулів сервера Apache.

### Приклади

**Приклад #1 Приклад використання** apache\_get\_modules()\*\*\*\*

```php
<?php
print_r(apache_get_modules());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => core
    [1] => http_core
    [2] => mod_so
    [3] => sapi_apache2
    [4] => mod_mime
    [5] => mod_rewrite
)
```
