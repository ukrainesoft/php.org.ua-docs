---
navigation:
  - simplexmliterator.haschildren.md: '« SimpleXMLIterator::hasChildren'
  - simplexmliterator.next.md: 'SimpleXMLIterator::next »'
  - index.md: PHP Manual
  - class.simplexmliterator.md: SimpleXMLIterator
title: 'SimpleXMLIterator::key'
---
# SimpleXMLIterator::key

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::key — Повертає поточний ключ

### Опис

```methodsynopsis
public SimpleXMLIterator::key(): mixed
```

Цей метод отримує ім'я тега XML поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я XML-тегу елемента, на який посилається поточний об'єкт [SimpleXMLIterator](class.simplexmliterator.md), або **`false`**

### Приклади

**Приклад #1 Отримує ім'я поточного тега XML**

```php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>Основы PHP</book><book>Основы XML</book></books>');

echo var_dump($xmlIterator->key());
$xmlIterator->rewind(); // возврат к первому элементу
echo var_dump($xmlIterator->key());

?>
```

Результат виконання цього прикладу:

```
bool(false)
string(4) "book"
```
