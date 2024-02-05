---
navigation:
  - ds-vector.jsonserialize.md: '« Ds\\Vector::jsonSerialize'
  - ds-vector.map.md: 'Ds\\Vector::map »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::last'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::last

(PECL ds >= 1.0.0)

Ds\\Vector::last — Повертає останнє значення вектора

### Опис

```methodsynopsis
public Ds\Vector::last(): mixed
```

Повертає останнє значення вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент вектор.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо вектор порожній.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::last()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->last());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
```
