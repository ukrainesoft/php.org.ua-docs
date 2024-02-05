---
navigation:
  - ref.spl.md: « Функції SPL
  - function.class-parents.md: class\_parents »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: class\_implements
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# class\_implements

(PHP 5, PHP 7, PHP 8)

class\_implements — Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі

### Опис

```methodsynopsis
class_implements(object|string $object_or_class, bool $autoload = true): array|false
```

Функція повертає масив імен інтерфейсів, реалізованих у заданому класі `object_or_class` та його батьківських класах.

### Список параметрів

`object_or_class`

Об'єкт (примірник класу) чи рядок (ім'я класу чи інтерфейсу).

`autoload`

Чи потрібно [автоматично підвантажувати](language.oop5.autoload.md) клас, якщо він ще не завантажений.

### Значення, що повертаються

У разі успішного виконання буде повернено масив, якщо заданий клас не існує, повертається **`false`**

### Приклади

**Пример #1 Пример использования**class\_implements()\*\*\*\*

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
    [interface_of_not_loaded] => interface_of_not_loaded
)
```

### Примітки

> **Зауваження**: Для перевірки того, що об'єкт реалізує інтерфейс, слід використовувати [`instanceof`](language.operators.type.md)или функцию[is\_a()](function.is-a.md)

### Дивіться також

-   [class\_parents()](function.class-parents.md) \- Повертає список батьківських класів заданого класу
-   [get\_declared\_interfaces()](function.get-declared-interfaces.md) \- Повертає масив усіх оголошених інтерфейсів
-   [is\_a()](function.is-a.md) \- Перевіряє, чи об'єкт належить до типу або підтипу
-   [`instanceof`](language.operators.type.md)
