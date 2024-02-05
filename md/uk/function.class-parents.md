---
navigation:
  - function.class-implements.md: « class\_implements
  - function.class-uses.md: class\_uses »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: class\_parents
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# class\_parents

(PHP 5, PHP 7, PHP 8)

class\_parents — Повертає список батьківських класів заданого класу

### Опис

```methodsynopsis
class_parents(object|string $object_or_class, bool $autoload = true): array|false
```

Ця функція повертає масив із іменами батьківських класів заданого класу `object_or_class`

### Список параметрів

`object_or_class`

Об'єкт (примірник класу) чи рядок (ім'я класу).

`autoload`

Чи потрібно [автоматично підвантажувати](language.oop5.autoload.md) клас, якщо він ще не завантажений.

### Значення, що повертаються

У разі успішного виконання буде повернено масив, якщо заданий клас не існує, повертається **`false`**

### Приклади

**Приклад #1 Приклад використання** class\_parents()\*\*\*\*

```php
<?php

class foo { }
class bar extends foo {}

print_r(class_parents(new bar));

// можно передавать имя класса вместо объекта
print_r(class_parents('bar'));


spl_autoload_register();

// использование автозагрузки для загрузки ещё незагруженного класса 'not_loaded'
print_r(class_parents('not_loaded', true));

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
    [parent_of_not_loaded] => parent_of_not_loaded
)
```

### Примітки

> **Зауваження**: Для перевірки того, що об'єкт реалізує інтерфейс, слід використовувати [`instanceof`](language.operators.type.md)или функцию[is\_a()](function.is-a.md)

### Дивіться також

-   [class\_implements()](function.class-implements.md) \- Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
-   [is\_a()](function.is-a.md) \- Перевіряє, чи об'єкт належить до типу або підтипу
-   [`instanceof`](language.operators.type.md)
