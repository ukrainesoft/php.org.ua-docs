---
navigation:
  - ds-map.put.html: '« DsMap::put'
  - ds-map.reduce.html: 'ДсMap::reduce »'
  - index.html: PHP Manual
  - class.ds-map.html: Коллекция пар ключ-значение
title: 'ДсMap::putAll'
---
# ДсMap::putAll

(PECL ds >= 1.0.2)

ДсMap::putAll — Зв'язує з колекцією всі пари ключ-значення з об'єкта класу traversable або масиву

### Опис

```methodsynopsis
public Ds\Map::putAll(mixed $pairs): void
```

Зв'язує з колекцією всі пари ключ-значення `pairs` з об'єкту класу [traversable](class.traversable.html) або array.

> **Зауваження**
> 
> Підтримуються значення типу об'єкта. Якщо об'єкт реалізує інтерфейс **ДсHashable**, перевірка здійснюється шляхом виклику методу об'єкта `equals`. Якщо об'єкт не реалізує інтерфейс **ДсHashable**, об'єкти повинні посилатися на той самий екземпляр класу.

### Список параметрів

`pairs`

Об'єкт класу [traversable](class.traversable.html) або array.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсMap::putAll()****

```php
<?php
$map = new \Ds\Map();

$map->putAll([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);

print_r($map);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 1
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 3
        )

)
```
