---
navigation:
  - function.uopz-allow-exit.md: « uopzallowexit
  - function.uopz-compose.md: uopzcompose »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzbackup
---
# uopzbackup

(PECL uopz 1> = 1.0.3, PECL uopz 2)

uopzbackup - Резервує функцію

**Увага**

Ця функція була *ВИДАЛЕНО* у PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_backup(string $function): void
```

```methodsynopsis
uopz_backup(string $class, string $function): void
```

Резервує функцію під час виконання, яка буде відновлена ​​після завершення роботи скрипту

### Список параметрів

`class`

Ім'я класу, що містить функцію для резервування

`function`

Ім'я функції

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **uopzbackup()****

```php
<?php
uopz_backup("fgets");
uopz_function("fgets", function(){
    return true;
});
var_dump(fgets());
?>
```

Результат виконання цього прикладу:

```
bool(true)
```
