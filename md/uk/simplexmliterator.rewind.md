---
navigation:
  - simplexmliterator.next.html: '« SimpleXMLIterator::next'
  - simplexmliterator.valid.html: 'SimpleXMLIterator::valid »'
  - index.html: PHP Manual
  - class.simplexmliterator.html: SimpleXMLIterator
title: 'SimpleXMLIterator::rewind'
---
# SimpleXMLIterator::rewind

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::rewind — Повертає ітератор до першого елементу

### Опис

```methodsynopsis
public SimpleXMLIterator::rewind(): void
```

Цей метод повертає [SimpleXMLIterator](class.simplexmliterator.html) до першого елементу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Повернення до першого елемента**

```php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>Основы PHP</book><book>Основы XML</book></books>');
$xmlIterator->rewind();

var_dump($xmlIterator->current());
?>
```

Результат виконання цього прикладу:

```
object(SimpleXMLIterator)#2 (1) {
  [0]=>
  string(10) "Основы PHP"
}
```
