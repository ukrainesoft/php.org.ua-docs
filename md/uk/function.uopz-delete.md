---
navigation:
  - function.uopz-del-function.md: « uopz\_del\_function
  - function.uopz-extend.md: uopz\_extend »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_delete

(PECL uopz 1, PECL uopz 2)

uopz\_delete — Видалити функцію

**Увага**

Ця функція була *ВИДАЛЕНО*в PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_delete(string $function): void
```

```methodsynopsis
uopz_delete(string $class, string $function): void
```

Видаляє функцію або метод

### Список параметрів

`class`

`function`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** uopz\_delete()\*\*\*\*

```php
<?php
uopz_delete("strlen");

echo strlen("Hello World");
?>
```

Висновок наведеного прикладу буде схожим на:

```
PHP Fatal error: Call to undefined function strlen() in /path/to/script.php on line 4
```

**Приклад #2 Приклад використання** uopz\_delete()\*\* з класом\*\*

```php
<?php
class My {
    public static function strlen($arg) {
        return strlen($arg);
    }
}

uopz_delete(My::class, "strlen");

echo My::strlen("Hello World");
?>
```

Висновок наведеного прикладу буде схожим на:

```
PHP Fatal error: Call to undefined method My::strlen() in /path/to/script.php on line 10
```
