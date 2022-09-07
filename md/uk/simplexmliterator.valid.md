---
navigation:
  - simplexmliterator.rewind.md: '« SimpleXMLIterator::rewind'
  - ref.simplexml.md: Функции SimpleXML »
  - index.md: PHP Manual
  - class.simplexmliterator.md: SimpleXMLIterator
title: 'SimpleXMLIterator::valid'
---
# SimpleXMLIterator::valid

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::valid — Перевіряє, чи поточний елемент є допустимим.

### Опис

```methodsynopsis
public SimpleXMLIterator::valid(): bool
```

Цей метод перевіряє, чи поточний елемент є допустимим після виклику [SimpleXMLIterator::rewind()](simplexmliterator.rewind.md) або [SimpleXMLIterator::next()](simplexmliterator.next.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо поточний елемент допустимо; в іншому випадку **`false`**

### Приклади

**Приклад #1 Перевіряє, чи поточний елемент є допустимим**

```php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>Основы SQL</book></books>');

$xmlIterator->rewind(); // возврат к первому элементу
echo var_dump($xmlIterator->valid()); // bool(true)

$xmlIterator->next(); // перейти к следующему элементу
echo var_dump($xmlIterator->valid()); // bool(false), поскольку есть только один элемент
?>
```
