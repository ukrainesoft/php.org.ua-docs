---
navigation:
  - cachingiterator.current.md: '« CachingIterator::current'
  - cachingiterator.getflags.md: 'CachingIterator::getFlags »'
  - index.md: PHP Manual
  - class.cachingiterator.md: CachingIterator
title: 'CachingIterator::getCache'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CachingIterator::getCache

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

CachingIterator::getCache — Отримання вмісту кешу

### Опис

```methodsynopsis
public CachingIterator::getCache(): array
```

Отримання вмісту кешу.

> **Зауваження** :
> 
> Має використовувати прапор **`CachingIterator::FULL_CACHE`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив array містить елементи кеша.

### Помилки

Викидає [BadMethodCallException](class.badmethodcallexception.md)в случае, если не установлен флаг\*\*`CachingIterator::FULL_CACHE`\*\*

### Приклади

**Приклад #1 Приклад використання** CachingIterator::getCache()\*\*\*\*

```php
<?php
$iterator = new ArrayIterator(array(1, 2, 3));
$cache    = new CachingIterator($iterator, CachingIterator::FULL_CACHE);

$cache->next();
$cache->next();
var_dump($cache->getCache());

$cache->next();
var_dump($cache->getCache());
?>
```

Результат виконання наведеного прикладу:

```
array(2) {
  [0]=>
  int(1)
  [1]=>
  int(2)
}
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
