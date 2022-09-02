---
navigation:
  - function.uopz-get-return.md: « uopzgetreturn
  - function.uopz-implement.md: uopzimplement »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzgetstatic
---
# uopzgetstatic

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzgetstatic — Повертає статичні змінні в області видимості функції або методу

### Опис

```methodsynopsis
uopz_get_static(string $class, string $function): array
```

```methodsynopsis
uopz_get_static(string $function): array
```

Повертає статичні змінні в області видимості функції або методу.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

### Значення, що повертаються

Повертає асоціативний масив (array) імен змінних, зіставлений зі своїми поточним значенням у разі успішного виконання, чи \*\*`null`\*\*якщо функція або метод не існують.

### Приклади

**Приклад #1 Просте використання **uopzgetstatic()****

```php
<?php
function foo() {
    static $bar = 'baz';
}
var_dump(uopz_get_static('foo'));
?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["bar"]=>
  string(3) "baz"
}
```

### Дивіться також

-   [uopzsetstatic()](function.uopz-set-static.md) - Встановлює статичні змінні у сфері видимості функції чи методу
