---
navigation:
  - function.uopz-undefine.html: « uopzundefine
  - function.uopz-unset-mock.html: uopzunsetmock »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzunsethook
---
# uopzunsethook

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzunsethook — Видалення попередньо встановленої функції або методу

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Просте використання **uopzunsethook()****

```php
<?php
function foo() {
    echo 'foo';
}
uopz_set_hook('foo', function () {echo 'bar';});
foo();
echo PHP_EOL;
uopz_unset_hook('foo');
foo();
?>
```

Результат виконання цього прикладу:

```
barfoo
foo
```

### Дивіться також

-   [uopzsethook()](function.uopz-set-hook.html) - Встановлює обробник для виконання під час виклику функції або методу
-   [uopzgethook()](function.uopz-get-hook.html) - отримує раніше встановлений обробник на функцію або метод
