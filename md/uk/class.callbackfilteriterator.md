---
navigation:
  - cachingiterator.valid.md: '« CachingIterator::valid'
  - callbackfilteriterator.accept.md: 'CallbackFilterIterator::accept »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас CallbackFilterIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас CallbackFilterIterator

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

    
     class CallbackFilterIterator
    

    
     extends
      FilterIterator
     {

    /* Методы */
    
   public __construct(Iterator $iterator, callable $callback)

    public accept(): bool


    /* Наследуемые методы */
    public FilterIterator::accept(): bool
public FilterIterator::current(): mixed
public FilterIterator::key(): mixed
public FilterIterator::next(): void
public FilterIterator::rewind(): void
public FilterIterator::valid(): bool

    public IteratorIterator::current(): mixed
public IteratorIterator::getInnerIterator(): ?Iterator
public IteratorIterator::key(): mixed
public IteratorIterator::next(): void
public IteratorIterator::rewind(): void
public IteratorIterator::valid(): bool

   }
```

## Приклади

Callback-функція може приймати до трьох аргументів: поточний елемент, поточний ключ та ітератор відповідно.

**Приклад #1 Доступні аргументи зворотного виклику**

```php
<?php

/**
 * Callback-функция для CallbackFilterIterator
 *
 * @param $current   Значение текущего элемента
 * @param $key       Ключ текущего элемента
 * @param $iterator  Фильтруемый итератор
 * @return boolean   TRUE для принятия текущего элемента, иначе - FALSE
 */
function my_callback($current, $key, $iterator) {
    // Код фильтрации
}

?>
```

Будь-яка callback-функція типу [callable](language.types.callable.md) може бути використана. Наприклад, рядок, який містить ім'я функції, масив для методу або анонімна функція.

**Приклад #2 Основні приклади зворотного виклику**

```php
<?php

$dir = new FilesystemIterator(__DIR__);

// Фильтр больших файлов ( > 100MB)
function is_large_file($current) {
    return $current->isFile() && $current->getSize() > 104857600;
}
$large_files = new CallbackFilterIterator($dir, 'is_large_file');

// Фильтр каталогов
$files = new CallbackFilterIterator($dir, function ($current, $key, $iterator) {
    return $current->isDir() && ! $iterator->isDot();
});

?>
```

## Зміст

-   [CallbackFilterIterator::accept](callbackfilteriterator.accept.md)— Викликає callback-функцію та передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик
-   [CallbackFilterIterator::\_\_construct](callbackfilteriterator.construct.md)— Створює ітератор, що фільтрує, на основі іншого ітератора.
