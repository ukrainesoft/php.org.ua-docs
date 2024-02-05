---
navigation:
  - function.uopz-get-return.md: « uopz\_get\_return
  - function.uopz-implement.md: uopz\_implement »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_get\_static
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_get\_static

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_get\_static — Повертає статичні змінні в області видимості функції або методу

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

**Пример #1 Простое использование**uopz\_get\_static()\*\*\*\*

```php
<?php
function foo() {
    static $bar = 'baz';
}
var_dump(uopz_get_static('foo'));
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["bar"]=>
  string(3) "baz"
}
```

### Дивіться також

-   [uopz\_set\_static()](function.uopz-set-static.md) \- Встановлює статичні змінні у сфері видимості функції чи методу
