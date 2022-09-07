---
navigation:
  - recursivecallbackfilteriterator.getchildren.md: '« RecursiveCallbackFilterIterator::getChildren'
  - class.recursivedirectoryiterator.md: RecursiveDirectoryIterator »
  - index.md: PHP Manual
  - class.recursivecallbackfilteriterator.md: RecursiveCallbackFilterIterator
title: 'RecursiveCallbackFilterIterator::hasChildren'
---
# RecursiveCallbackFilterIterator::hasChildren

(PHP 5> = 5.4.0, PHP 7, PHP 8)

RecursiveCallbackFilterIterator::hasChildren — Перевіряє, чи містить поточний елемент внутрішнього ітератора дочірні елементи

### Опис

```methodsynopsis
public RecursiveCallbackFilterIterator::hasChildren(): bool
```

Повертає **`true`**, якщо поточний елемент має дочірні елементи і **`false`**, якщо ні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо поточний елемент має дочірні елементи і **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання **RecursiveCallbackFilterIterator::hasChildren()****

```php
<?php

$dir = new RecursiveDirectoryIterator(__DIR__);

// Рекурсивный обход XML файлов
$files = new RecursiveCallbackFilterIterator($dir, function ($current, $key, $iterator) {
    // просматривать директории
    if ($iterator->hasChildren()) {
        return TRUE;
    }
    // отбор XML файлов
    if (!strcasecmp($current->getExtension(), 'xml')) {
        return TRUE;
    }
    return FALSE;
});

?>
```

### Дивіться також

-   [Приклади використання RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.md#recursivecallbackfilteriterator.examples)
-   [RecursiveCallbackFilterIterator::construct()](recursivecallbackfilteriterator.construct.md) - Створює об'єкт класу RecursiveCallbackFilterIterator на основі об'єкта RecursiveIterator
-   [RecursiveCallbackFilteriterator::getChildren()](recursivecallbackfilteriterator.getchildren.md) - Повертає дочірні елементи ітератора, що зберігається всередині RecursiveCallbackFilterIterator
