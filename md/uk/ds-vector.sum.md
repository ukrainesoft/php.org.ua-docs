---
navigation:
  - ds-vector.sorted.md: '« Ds\\Vector::sorted'
  - ds-vector.toarray.md: 'Ds\\Vector::toArray »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::sum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::sum

(PECL ds >= 1.0.0)

Ds\\Vector::sum — Повертає суму всіх значень колекції

### Опис

```methodsynopsis
public Ds\Vector::sum(): int|float
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

**Пример #1 Пример использования**Ds\\Vector::sum()\*\* з цілими значеннями\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(6)
```

**Пример #2 Пример использования**Ds\\Vector::sum()\*\* зі значеннями типу float\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2.5, 3]);
var_dump($vector->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
float(6.5)
```
