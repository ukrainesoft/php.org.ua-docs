---
navigation:
  - ds-vector.merge.md: '« Ds\\Vector::merge'
  - ds-vector.push.md: 'Ds\\Vector::push »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::pop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::pop

(PECL ds >= 1.0.0)

Ds\\Vector::pop — Видаляє та повертає останнє значення

### Опис

```methodsynopsis
public Ds\Vector::pop(): mixed
```

Видаляє та повертає останнє значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останнє віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо вектор порожній.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::pop()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->pop());
var_dump($vector->pop());
var_dump($vector->pop());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
int(2)
int(1)
```
