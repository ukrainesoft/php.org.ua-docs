---
navigation:
  - ds-set.add.md: '« Ds\\Set::add'
  - ds-set.capacity.md: 'Ds\\Set::capacity »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::allocate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::allocate

(PECL ds >= 1.0.0)

Ds\\Set::allocate — Виділяє пам'ять під зазначену місткість

### Опис

```methodsynopsis
public Ds\Set::allocate(int $capacity): void
```

Виділяє пам'ять під зазначену місткість.

### Список параметрів

`capacity`

Місткість. Очікувана кількість значень.

> **Зауваження** :
> 
> Якщо нове значення місткості менше поточного, воно не зміниться.

> **Зауваження** :
> 
> Значення місткості округляється до найближчого ступеня двійки (тобто 8, 16, 32, 64, 128 і т.д.)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Set::allocate()\*\*\*\*

```php
<?php
$set = new \Ds\Set();
var_dump($set->capacity());

$set->allocate(100);
var_dump($set->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(16)
int(128)
```
