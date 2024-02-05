---
navigation:
  - ds-pair.jsonserialize.md: '« Ds\\Pair::jsonSerialize'
  - class.ds-set.md: Ds\\Set »
  - index.md: PHP Manual
  - class.ds-pair.md: Ds\\Pair
title: 'Ds\\Pair::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Pair::toArray

(PECL ds >= 1.0.0)

Ds\\Pair::toArray - Перетворює пару в масив (array)

### Опис

```methodsynopsis
public Ds\Pair::toArray(): array
```

Перетворює пару на масив (array).

> **Зауваження** :
> 
> Приведення до масиву поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив містить елементи в тому ж порядку, як вони були в парі.

### Приклади

**Приклад #1 Приклад використання** Ds\\Pair::toArray()\*\*\*\*

```php
<?php
$pair = new \Ds\Pair("a", 1);

var_dump($pair->toArray());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(2) {
  ["key"]=>
  string(1) "a"
  ["value"]=>
  int(1)
}
```
