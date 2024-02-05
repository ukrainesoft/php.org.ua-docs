---
navigation:
  - ds-map.sorted.md: '« Ds\\Map::sorted'
  - ds-map.toarray.md: 'Ds\\Map::toArray »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::sum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::sum

(No version information available, might only be in Git)

Ds\\Map::sum — Повертає суму всіх значень колекції

### Опис

```methodsynopsis
public Ds\Map::sum(): int|float
```

Повертає суму всіх значень колекції.

> **Зауваження** :
> 
> Масиви та об'єкти вважаються нулем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Сума всіх значень колекції типу float або int, залежно від значень колекції.

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::sum()\*\* з цілими значеннями\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(6)
```

**Приклад #2 Приклад використання** Ds\\Map::sum()\*\* зі значеннями типу float\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2.5, "c" => 3]);
var_dump($map->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
float(6.5)
```
