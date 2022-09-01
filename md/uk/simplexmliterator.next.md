---
navigation:
  - simplexmliterator.key.md: '« SimpleXMLIterator::key'
  - simplexmliterator.rewind.md: 'SimpleXMLIterator::rewind »'
  - index.md: PHP Manual
  - class.simplexmliterator.md: SimpleXMLIterator
title: 'SimpleXMLIterator::next'
---
# SimpleXMLIterator::next

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::next — Переміщення ітератора до наступного елемента

### Опис

```methodsynopsis
public SimpleXMLIterator::next(): void
```

Цей метод переміщує [SimpleXMLIterator](class.simplexmliterator.md) до наступного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Переміщення до наступного елементу**

```php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>Основы PHP</book><book>Основы XML</book></books>');
$xmlIterator->rewind(); // возврат к первому элементу
$xmlIterator->next();

var_dump($xmlIterator->current());
?>
```

Результат виконання цього прикладу:

```
object(SimpleXMLIterator)#2 (1) {
  [0]=>
  string(10) "Основы XML"
}
```
