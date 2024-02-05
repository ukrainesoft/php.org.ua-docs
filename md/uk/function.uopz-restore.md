---
navigation:
  - function.uopz-rename.md: « uopz\_rename
  - function.uopz-set-hook.md: uopz\_set\_hook »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_restore
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_restore

(PECL uopz 1 >= 1.0.3, PECL uopz 2)

uopz\_restore — Відновити раніше зарезервовану функцію

**Увага**

Ця функція була *ВИДАЛЕНО*в PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_restore(string $function): void
```

```methodsynopsis
uopz_restore(string $class, string $function): void
```

Відновити раніше зарезервовану функцію

### Список параметрів

`class`

Ім'я класу, що містить функцію відновлення

`function`

Ім'я функції

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** uopz\_restore()\*\*\*\*

```php
<?php
uopz_backup("fgets");
uopz_function("fgets", function(){
    return true;
});
var_dump(fgets());
uopz_restore('fgets');
fgets();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Warning: fgets() expects at least 1 parameter, 0 given in /path/to/script.php on line 8
```
