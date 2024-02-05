---
navigation:
  - function.class-parents.md: « class\_parents
  - function.iterator-apply.md: iterator\_apply »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: class\_uses
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# class\_uses

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

class\_uses — Повертає список трейтів, що використовуються заданим класом

### Опис

```methodsynopsis
class_uses(object|string $object_or_class, bool $autoload = true): array|false
```

Ця функція повертає масив із іменами трейтів, які використовує заданий клас `object_or_class`. У цей масив, однак, не потраплять трейти, які використовуються у класах-батьках.

### Список параметрів

`object_or_class`

Об'єкт (примірник класу) чи рядок (ім'я класу).

`autoload`

Чи потрібно [автоматично підвантажувати](language.oop5.autoload.md) клас, якщо він ще не завантажений.

### Значення, що повертаються

У разі успішного виконання буде повернено масив, якщо заданий клас не існує, повертається **`false`**

### Приклади

**Пример #1 Пример использования**class\_uses()\*\*\*\*

```php
<?php

trait foo { }
class bar {
  use foo;
}

print_r(class_uses(new bar));

print_r(class_uses('bar'));

spl_autoload_register();

// использование автозагрузки для загрузки ещё незагруженного класса 'not_loaded'
print_r(class_uses('not_loaded', true));

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [class\_parents()](function.class-parents.md) \- Повертає список батьківських класів заданого класу
-   [get\_declared\_traits()](function.get-declared-traits.md) \- Повертає масив з усіма оголошеними трейтами
