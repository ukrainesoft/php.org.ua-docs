---
navigation:
  - function.class-parents.md: « classparents
  - function.iterator-apply.md: iteratorapply »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: classuses
---
# classuses

(PHP 5> = 5.4.0, PHP 7, PHP 8)

classuses — Повертає список трейтів, що використовуються заданим класом

### Опис

```methodsynopsis
class_uses(object|string $object_or_class, bool $autoload = true): array|false
```

Ця функція повертає масив із іменами трейтів, які використовує заданий клас `object_or_class`. У цей масив, однак, не потраплять трейти, які використовуються у класах-батьках.

### Список параметрів

`object_or_class`

Об'єкт (примірник класу) чи рядок (ім'я класу).

`autoload`

Чи викликати за замовчуванням [autoload](language.oop5.autoload.md)

### Значення, що повертаються

У разі успішного виконання буде повернено масив, якщо заданий клас не існує, повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **classuses()****

```php
<?php

trait foo { }
class bar {
  use foo;
}

print_r(class_uses(new bar));

print_r(class_uses('bar'));

spl_autoload_register();

// использование автозагрузки для загрузки ещё незагруженного класса 'not_loaded'
print_r(class_uses('not_loaded', true));

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
    [trait_of_not_loaded] => trait_of_not_loaded
)
```

### Дивіться також

-   [classparents()](function.class-parents.md) - Повертає список батьківських класів заданого класу
-   [getdeclaredtraits()](function.get-declared-traits.md) - Повертає масив з усіма оголошеними трейтами
