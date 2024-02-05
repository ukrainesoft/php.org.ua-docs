---
navigation:
  - function.uopz-restore.md: « uopz\_restore
  - function.uopz-set-mock.md: uopz\_set\_mock »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_set\_hook
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_set\_hook

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_set\_hook — Встановлює обробник для виконання під час виклику функції або методу

### Опис

```methodsynopsis
uopz_set_hook(string $function, Closure $hook): bool
```

```methodsynopsis
uopz_set_hook(string $class, string $function, Closure $hook): bool
```

Встановлює обробник для виконання під час виклику функції або методу.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

`hook`

Замикання, яке виконується під час виклику функції або методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Простое использование**uopz\_set\_hook()\*\*\*\*

```php
<?php
function foo() {
    echo 'foo';
}
uopz_set_hook('foo', function () {echo 'bar';});
foo();
?>
```

Результат виконання наведеного прикладу:

```
barfoo
```

### Дивіться також

-   [uopz\_get\_hook()](function.uopz-get-hook.md) \- отримує раніше встановлений обробник на функцію або метод
-   [uopz\_unset\_hook()](function.uopz-unset-hook.md) \- Видаляє раніше встановлену функцію чи метод
