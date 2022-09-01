---
navigation:
  - function.apache-get-modules.html: « apachegetmodules
  - function.apache-getenv.html: apachegetenv »
  - index.html: PHP Manual
  - ref.apache.html: Функции Apache
title: apachegetversion
---
# apachegetversion

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

apachegetversion — Повертає версію Apache

### Опис

```methodsynopsis
apache_get_version(): string|false
```

Повертає версію Apache.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає версію Apache або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apachegetversion()****

```php
<?php
$version = apache_get_version();
echo "$version\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Apache/1.3.29 (Unix) PHP/4.3.4
```

### Дивіться також

-   [phpinfo()](function.phpinfo.md) - Виводить інформацію про поточну конфігурацію PHP
