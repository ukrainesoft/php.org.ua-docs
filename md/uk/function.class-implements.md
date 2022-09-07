---
navigation:
  - ref.spl.md: « Функції SPL
  - function.class-parents.md: classparents »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: classimplements
---
# classimplements

(PHP 5, PHP 7, PHP 8)

classimplements — Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі

### Опис

```methodsynopsis
class_implements(object|string $object_or_class, bool $autoload = true): array|false
```

Функція повертає масив імен інтерфейсів, реалізованих у заданому класі `object_or_class` та його батьківських класах.

### Список параметрів

`object_or_class`

Об'єкт (примірник класу) чи рядок (ім'я класу чи інтерфейсу).

`autoload`

Чи викликати за замовчуванням [autoload](language.oop5.autoload.md)

### Значення, що повертаються

У разі успішного виконання буде повернено масив, якщо заданий клас не існує, повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **classimplements()****

```php
<?php

interface foo { }
class bar implements foo {}

print_r(class_implements(new bar));

// можно передавать имя класса вместо объекта
print_r(class_implements('bar'));


spl_autoload_register();

// использование автозагрузки для загрузки ещё незагруженного класса 'not_loaded'
print_r(class_implements('not_loaded', true));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [foo] => foo
)
Array
(
    [foo] => foo
)
Array
(
    [interface_of_not_loaded] => interface_of_not_loaded
)
```

### Дивіться також

-   [classparents()](function.class-parents.md) - Повертає список батьківських класів заданого класу
-   [getdeclaredinterfaces()](function.get-declared-interfaces.md) - Повертає масив усіх оголошених інтерфейсів
