---
navigation:
  - ds-map.put.md: '« Ds\\Map::put'
  - ds-map.reduce.md: 'Ds\\Map::reduce »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::putAll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::putAll

(PECL ds >= 1.0.2)

Ds\\Map::putAll — Зв'язує з колекцією всі пари ключ-значення з об'єкта класу traversable або масиву

### Опис

```methodsynopsis
public Ds\Map::putAll(mixed $pairs): void
```

Зв'язує з колекцією всі пари ключ-значення `pairs` з об'єкту класу [traversable](class.traversable.md)или array.

> **Зауваження** :
> 
> Підтримуються значення типу об'єкта. Якщо об'єкт реалізує інтерфейс [Ds\\Hashable](class.ds-hashable.md), перевірка здійснюється шляхом виклику методу об'єкта `equals`. Якщо об'єкт не реалізує інтерфейс [Ds\\Hashable](class.ds-hashable.md), об'єкти повинні посилатися на той самий екземпляр класу.

### Список параметрів

`pairs`

Об'єкт класу [traversable](class.traversable.md)или array.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Map::putAll()\*\*\*\*

```php
<?php
$map = new \Ds\Map();

$map->putAll([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);

print_r($map);
?>
```

Висновок наведеного прикладу буде схожим на:

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
