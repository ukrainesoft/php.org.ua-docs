---
navigation:
  - function.uopz-set-return.md: « uopzsetreturn
  - function.uopz-undefine.md: uopzundefine »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzsetstatic
---
# uopzsetstatic

(PECL uopz 5, PECL uopz, PECL uopz 7)

uopzsetstatic - Встановлює статичні змінні в області видимості функції або методу

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

**Приклад #1 Просте використання **uopzsetstatic()****

```php
<?php
function foo() {
    static $bar = 'baz';
    var_dump($bar);
}
uopz_set_static('foo', ['bar' => 'qux']);
foo();
?>
```

Результат виконання цього прикладу:

```
string(3) "qux"
```

### Дивіться також

-   [uopzgetstatic()](function.uopz-get-static.md) - Повертає статичні змінні в області видимості функції або методу
