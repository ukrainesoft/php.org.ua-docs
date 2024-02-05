---
navigation:
  - class.ds-sequence.md: « Ds\\Sequence
  - ds-sequence.apply.md: 'Ds\\Sequence::apply »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::allocate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::allocate

(PECL ds >= 1.0.0)

Ds\\Sequence::allocate — Виділення пам'яті під зазначену місткість

### Опис

```methodsynopsis
abstract public Ds\Sequence::allocate(int $capacity): void
```

Гарантує, що виділено достатньо пам'яті під задану місткість (кількість значень). Дозволяє уникнути динамічного додавання пам'яті під час додавання значень.

### Список параметрів

`capacity`

Місткість. Очікувана кількість значень.

> **Зауваження** :
> 
> Якщо нове значення місткості менше поточного, вона не зміниться.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::allocate()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector();
var_dump($sequence->capacity());

$vector->allocate(100);
var_dump($sequence->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(10)
int(100)
```
