---
navigation:
  - recursivecallbackfilteriterator.construct.md: '« RecursiveCallbackFilterIterator::\_\_construct'
  - recursivecallbackfilteriterator.haschildren.md: 'RecursiveCallbackFilterIterator::hasChildren »'
  - index.md: PHP Manual
  - class.recursivecallbackfilteriterator.md: RecursiveCallbackFilterIterator
title: 'RecursiveCallbackFilterIterator::getChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveCallbackFilterIterator::getChildren

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

RecursiveCallbackFilterIterator::getChildren — Повертає дочірні елементи ітератора, що зберігається всередині RecursiveCallbackFilterIterator

### Опис

```methodsynopsis
public RecursiveCallbackFilterIterator::getChildren(): RecursiveCallbackFilterIterator
```

Вибирає дочірні елементи внутрішнього ітератора, які підходять під фільтрові умови.

Перш ніж викликати метод, необхідно впевнитись, що внутрішній ітератор містить дочірні елементи. Зробити це можна за допомогою методу [RecursiveCallbackFilterIterator::hasChildren()](recursivecallbackfilteriterator.haschildren.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.md)містить дочірні елементи внутрішнього ітератора.

### Дивіться також

-   [Приклади використання RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.md#recursivecallbackfilteriterator.examples)
-   [RecursiveCallbackFilterIterator::\_\_construct()](recursivecallbackfilteriterator.construct.md) \- Створює об'єкт класу RecursiveCallbackFilterIterator на основі об'єкта RecursiveIterator
-   [RecursiveCallbackFilteriterator::hasChildren()](recursivecallbackfilteriterator.haschildren.md) \- Перевіряє, чи містить поточний елемент внутрішнього ітератора дочірні елементи
