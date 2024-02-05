---
navigation:
  - ds-vector.find.md: '« Ds\\Vector::find'
  - ds-vector.get.md: 'Ds\\Vector::get »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::first'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::first

(PECL ds >= 1.0.0)

Ds\\Vector::first — Повертає перший елемент вектора

### Опис

```methodsynopsis
public Ds\Vector::first(): mixed
```

Повертає перший елемент вектор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент вектор.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо вектор порожній.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::first()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->first());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
```
