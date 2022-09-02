---
navigation:
  - class.ds-vector.md: « Вектор
  - ds-vector.apply.md: 'ДсVector::apply »'
  - index.md: PHP Manual
  - class.ds-vector.md: Вектор
title: 'ДсVector::allocate'
---
# ДсVector::allocate

(PECL ds >= 1.0.0)

ДсVector::allocate — Виділяє пам'ять під зазначену місткість

### Опис

```methodsynopsis
public Ds\Vector::allocate(int $capacity): void
```

Гарантує, що виділено достатньо пам'яті під задану місткість (кількість значень). Дозволяє уникнути динамічного перерозподілу пам'яті під час додавання значень.

### Список параметрів

`capacity`

Місткість. Очікувана кількість значень.

> **Зауваження**
> 
> Місткість залишиться незмінною, якщо її значення менше або дорівнює поточній місткості.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::allocate()****

```php
<?php
$vector = new \Ds\Vector();
var_dump($vector->capacity());

$vector->allocate(100);
var_dump($vector->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(10)
int(100)
```
