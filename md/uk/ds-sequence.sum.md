---
navigation:
  - ds-sequence.sorted.md: '« Ds\\Sequence::sorted'
  - ds-sequence.unshift.md: 'Ds\\Sequence::unshift »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::sum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::sum

(PECL ds >= 1.0.0)

Ds\\Sequence::sum — Повертає суму всіх значень колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::sum(): int|float
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

**Пример #1 Пример использования**Ds\\Sequence::sum()\*\* з цілими значеннями\*\*

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(6)
```

**Пример #2 Пример использования**Ds\\Sequence::sum()\*\* зі значеннями типу float\*\*

```php
<?php
$sequence = new \Ds\Vector([1, 2.5, 3]);
var_dump($sequence->sum());
?>
```

Висновок наведеного прикладу буде схожим на:

```
float(6.5)
```
