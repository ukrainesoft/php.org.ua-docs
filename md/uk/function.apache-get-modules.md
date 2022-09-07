---
navigation:
  - function.apache-child-terminate.md: « apachechildterminate
  - function.apache-get-version.md: apachegetversion »
  - index.md: PHP Manual
  - ref.apache.md: Функции Apache
title: apachegetmodules
---
# apachegetmodules

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

apachegetmodules — Повертає список завантажених модулів сервера Apache

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

**Приклад #1 Приклад використання **apachegetmodules()****

```php
<?php
print_r(apache_get_modules());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
