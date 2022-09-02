---
navigation:
  - function.uopz-get-exit-status.md: « uopzgetexitstatus
  - function.uopz-get-mock.md: uopzgetmock »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzgethook
---
# uopzgethook

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzgethook — Отримує раніше встановлений обробник на функцію або метод

### Опис

```methodsynopsis
uopz_get_hook(string $function): Closure
```

```methodsynopsis
uopz_get_hook(string $class, string $function): Closure
```

Отримує встановлений обробник на функцію або метод.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

### Значення, що повертаються

Повертає раніше встановлений обробник на функцію або метод, або \*\*`null`\*\*якщо обробник не був встановлений.

### Приклади

**Приклад #1 Просте використання **uopzgethook()****

```php
<?php
function foo() {
    echo 'foo';
}
uopz_set_hook('foo', function () {echo 'bar';});
var_dump(uopz_get_hook('foo'));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Closure)#2 (0) {
}
```

### Дивіться також

-   [uopzsethook()](function.uopz-set-hook.md) - Встановлює обробник для виконання під час виклику функції або методу
-   [uopzunsethook()](function.uopz-unset-hook.md) - Видаляє раніше встановлену функцію чи метод
