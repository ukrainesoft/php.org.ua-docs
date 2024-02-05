---
navigation:
  - function.uopz-get-exit-status.md: « uopz\_get\_exit\_status
  - function.uopz-get-mock.md: uopz\_get\_mock »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_get\_hook
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_get\_hook

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_get\_hook — Отримує раніше встановлений обробник на функцію або метод

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

**Пример #1 Простое использование**uopz\_get\_hook()\*\*\*\*

```php
<?php
function foo() {
    echo 'foo';
}
uopz_set_hook('foo', function () {echo 'bar';});
var_dump(uopz_get_hook('foo'));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Closure)#2 (0) {
}
```

### Дивіться також

-   [uopz\_set\_hook()](function.uopz-set-hook.md) \- Встановлює обробник для виконання під час виклику функції або методу
-   [uopz\_unset\_hook()](function.uopz-unset-hook.md) \- Видаляє раніше встановлену функцію чи метод
