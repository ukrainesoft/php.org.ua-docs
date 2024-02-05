---
navigation:
  - class.ds-vector.md: « Ds\\Vector
  - ds-vector.apply.md: 'Ds\\Vector::apply »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::allocate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::allocate

(PECL ds >= 1.0.0)

Ds\\Vector::allocate — Виділяє пам'ять під зазначену місткість

### Опис

```methodsynopsis
public Ds\Vector::allocate(int $capacity): void
```

Гарантує, що виділено достатньо пам'яті під задану місткість (кількість значень). Дозволяє уникнути динамічного перерозподілу пам'яті під час додавання значень.

### Список параметрів

`capacity`

Місткість. Очікувана кількість значень.

> **Зауваження** :
> 
> Місткість залишиться незмінною, якщо її значення менше або дорівнює поточній місткості.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::allocate()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector();
var_dump($vector->capacity());

$vector->allocate(100);
var_dump($vector->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(10)
int(100)
```
