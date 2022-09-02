---
navigation:
  - function.uopz-del-function.md: « uopzdelfunction
  - function.uopz-extend.md: uopzextend »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzdelete
---
# uopzdelete

(PECL uopz 1, PECL uopz 2)

uopzdelete — Видалити функцію

**Увага**

Ця функція була *ВИДАЛЕНО* у PECL uopz 5.0.0.

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

**Приклад #1 Приклад використання **uopzdelete()****

```php
<?php
uopz_delete("strlen");

echo strlen("Hello World");
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
PHP Fatal error: Call to undefined function strlen() in /path/to/script.php on line 4
```

**Приклад #2 Приклад використання **uopzdelete()** з класом**

```php
<?php
class My {
    public static function strlen($arg) {
        return strlen($arg);
    }
}

uopz_delete(My::class, "strlen");

echo My::strlen("Hello World");
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
PHP Fatal error: Call to undefined method My::strlen() in /path/to/script.php on line 10
```
