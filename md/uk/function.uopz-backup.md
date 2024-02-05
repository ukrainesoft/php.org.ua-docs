---
navigation:
  - function.uopz-allow-exit.md: « uopz\_allow\_exit
  - function.uopz-compose.md: uopz\_compose »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_backup
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_backup

(PECL uopz 1 >= 1.0.3, PECL uopz 2)

uopz\_backup - Резервує функцію

**Увага**

Ця функція була *ВИДАЛЕНО*в PECL uopz 5.0.0.

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

**Пример #1 Пример использования**uopz\_backup()\*\*\*\*

```php
<?php
uopz_backup("fgets");
uopz_function("fgets", function(){
    return true;
});
var_dump(fgets());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
