---
navigation:
  - function.uopz-set-return.md: « uopz\_set\_return
  - function.uopz-undefine.md: uopz\_undefine »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_set\_static
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_set\_static

(PECL uopz 5, PECL uopz , PECL uopz 7)

uopz\_set\_static - Встановлює статичні змінні в області видимості функції або методу

### Опис

```methodsynopsis
uopz_set_static(string $function, array $static): void
```

```methodsynopsis
uopz_set_static(string $class, string $function, array $static): void
```

Встановлює статичні змінні у сфері видимості функції чи методу.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

`static`

Асоціативний масив (array) імен змінних, зіставлених зі своїми значеннями.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Простое использование**uopz\_set\_static()\*\*\*\*

```php
<?php
function foo() {
    static $bar = 'baz';
    var_dump($bar);
}
uopz_set_static('foo', ['bar' => 'qux']);
foo();
?>
```

Результат виконання наведеного прикладу:

```
string(3) "qux"
```

### Дивіться також

-   [uopz\_get\_static()](function.uopz-get-static.md) \- Повертає статичні змінні в області видимості функції або методу
