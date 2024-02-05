---
navigation:
  - function.uopz-undefine.md: « uopz\_undefine
  - function.uopz-unset-mock.md: uopz\_unset\_mock »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_unset\_hook
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_unset\_hook

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_unset\_hook — Видалення попередньо встановленої функції або методу

### Опис

```methodsynopsis
uopz_unset_hook(string $function): bool
```

```methodsynopsis
uopz_unset_hook(string $class, string $function): bool
```

Видаляє раніше встановлену функцію чи метод.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Простое использование**uopz\_unset\_hook()\*\*\*\*

```php
<?php
function foo() {
    echo 'foo';
}
uopz_set_hook('foo', function () {echo 'bar';});
foo();
echo PHP_EOL;
uopz_unset_hook('foo');
foo();
?>
```

Результат виконання наведеного прикладу:

```
barfoo
foo
```

### Дивіться також

-   [uopz\_set\_hook()](function.uopz-set-hook.md) \- Встановлює обробник для виконання під час виклику функції або методу
-   [uopz\_get\_hook()](function.uopz-get-hook.md) \- отримує раніше встановлений обробник на функцію або метод
