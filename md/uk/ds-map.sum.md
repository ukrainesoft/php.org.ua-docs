---
navigation:
  - ds-map.sorted.html: '« DsMap::sorted'
  - ds-map.toarray.html: 'ДсMap::toArray »'
  - index.md: PHP Manual
  - class.ds-map.html: Коллекция пар ключ-значение
title: 'ДсMap::sum'
---
# ДсMap::sum

(No version information available, might only be in Git)

ДсMap::sum — Повертає суму всіх значень колекції

### Опис

```methodsynopsis
public Ds\Map::sum(): int|float
```

Повертає суму всіх значень колекції.

> **Зауваження**
> 
> Масиви та об'єкти вважаються нулем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Сума всіх значень колекції типу float або int, залежно від значень колекції.

### Приклади

**Приклад #1 Приклад використання **ДсMap::sum()** з цілими значеннями**

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->sum());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(6)
```

**Приклад #2 Приклад використання **ДсMap::sum()** зі значеннями типу float**

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2.5, "c" => 3]);
var_dump($map->sum());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
float(6.5)
```
