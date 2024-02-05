---
navigation:
  - ds-set.sorted.md: '« Ds\\Set::sorted'
  - ds-set.toarray.md: 'Ds\\Set::toArray »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::sum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::sum

(PECL ds >= 1.0.0)

Ds\\Set::sum — Повертає суму всіх значень колекції

### Опис

```methodsynopsis
public Ds\Set::sum(): int|float
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

**Пример #1 Пример использования**Ds\\Set::sum()\*\* з цілими значеннями\*\*

```php
<?php
$set = new \Ds\Set([1, 2, 3]);
var_dump($set->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(6)
```

**Пример #2 Пример использования**Ds\\Set::sum()\*\* зі значеннями типу float\*\*

```php
<?php
$set = new \Ds\Set([1, 2.5, 3]);
var_dump($set->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
float(6.5)
```
