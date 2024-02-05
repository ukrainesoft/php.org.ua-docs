---
navigation:
  - ds-deque.first.md: '« Ds\\Deque::first'
  - ds-deque.insert.md: 'Ds\\Deque::insert »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::get

(PECL ds >= 1.0.0)

Ds\\Deque::get — Повертає значення за індексом

### Опис

```methodsynopsis
public Ds\Deque::get(int $index): mixed
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

**Пример #1 Пример использования**Ds\\Deque::get()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->get(0));
var_dump($deque->get(1));
var_dump($deque->get(2));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

**Пример #2 Пример использования**Ds\\Deque::get()\*\* із синтаксисом масиву\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque[0]);
var_dump($deque[1]);
var_dump($deque[2]);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
