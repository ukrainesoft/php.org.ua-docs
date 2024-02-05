---
navigation:
  - function.apache-get-modules.md: « apache\_get\_modules
  - function.apache-getenv.md: apache\_getenv »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_get\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_get\_version

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

apache\_get\_version — Повертає версію Apache

### Опис

```methodsynopsis
apache_get_version(): string|false
```

Повертає версію Apache.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає версію Apache або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** apache\_get\_version()\*\*\*\*

```php
<?php
$version = apache_get_version();
echo "$version\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
Apache/1.3.29 (Unix) PHP/4.3.4
```

### Дивіться також

-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
