---
navigation:
  - ds-set.filter.html: '« DsSet::filter'
  - ds-set.get.html: 'ДсSet::get »'
  - index.html: PHP Manual
  - class.ds-set.html: Набор
title: 'ДсSet::first'
---
# ДсSet::first

(PECL ds >= 1.0.0)

ДсSet::first — Повертає перший елемент колекції

### Опис

```methodsynopsis
public Ds\Set::first(): mixed
```

Повертає перший елемент колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсSet::first()****

```php
<?php
$set = new \Ds\Set([1, 2, 3]);
var_dump($set->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
```
