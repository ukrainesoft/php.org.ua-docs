---
navigation:
  - function.class-implements.html: « classimplements
  - function.class-uses.html: classuses »
  - index.html: PHP Manual
  - ref.spl.html: Функції SPL
title: classparents
---
# classparents

(PHP 5, PHP 7, PHP 8)

classparents — Повертає список батьківських класів заданого класу

### Опис

```methodsynopsis
class_parents(object|string $object_or_class, bool $autoload = true): array|false
```

Ця функція повертає масив із іменами батьківських класів заданого класу `object_or_class`

### Список параметрів

`object_or_class`

Об'єкт (примірник класу) чи рядок (ім'я класу).

`autoload`

Чи викликати за замовчуванням [autoload](language.oop5.autoload.html)

### Значення, що повертаються

У разі успішного виконання буде повернено масив, якщо заданий клас не існує, повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **classparents()****

```php
<?php

class foo { }
class bar extends foo {}

print_r(class_parents(new bar));

// можно передавать имя класса вместо объекта
print_r(class_parents('bar'));


spl_autoload_register();

// использование автозагрузки для загрузки ещё незагруженного класса 'not_loaded'
print_r(class_parents('not_loaded', true));

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
    [parent_of_not_loaded] => parent_of_not_loaded
)
```

### Дивіться також

-   [classimplements()](function.class-implements.html) - Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
