---
navigation:
  - ds-set.first.md: '« Ds\\Set::first'
  - ds-set.intersect.md: 'Ds\\Set::intersect »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::get

(PECL ds >= 1.0.0)

Ds\\Set::get — Повертає значення за індексом

### Опис

```methodsynopsis
public Ds\Set::get(int $index): mixed
```

Повертає значення за заданим індексом.

### Список параметрів

`index`

Індекс. Перший елемент має індекс 0.

### Значення, що повертаються

Значення за заданим індексом.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Пример #1 Пример использования**Ds\\Set::get()\*\*\*\*

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

var_dump($set->get(0));
var_dump($set->get(1));
var_dump($set->get(2));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

**Пример #2 Пример использования**Ds\\Set::get()\*\* із синтаксисом масиву\*\*

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

var_dump($set[0]);
var_dump($set[1]);
var_dump($set[2]);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
