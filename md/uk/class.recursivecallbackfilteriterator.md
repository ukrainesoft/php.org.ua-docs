---
navigation:
  - recursivecachingiterator.haschildren.md: '« RecursiveCachingIterator::hasChildren'
  - recursivecallbackfilteriterator.construct.md: 'RecursiveCallbackFilterIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас RecursiveCallbackFilterIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас RecursiveCallbackFilterIterator

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

    
     class RecursiveCallbackFilterIterator
    

    
     extends
      CallbackFilterIterator
    

    
     implements
      RecursiveIterator {

    /* Методы */
    
   public __construct(RecursiveIterator $iterator, callable $callback)

    public getChildren(): RecursiveCallbackFilterIterator
public hasChildren(): bool


    /* Наследуемые методы */
    public CallbackFilterIterator::accept(): bool

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

**Приклад #1 Доступні аргументи callback-функції**

```php
<?php

/**
 * Callback-функция для RecursiveCallbackFilterIterator
 *
 * @param $current   Значение текущего элемента
 * @param $key       Ключ текущего элемента
 * @param $iterator  Итератор, который фильтруется
 * @return boolean   TRUE для приёма текущего элемента или FALSE - в ином случае.
 */
function my_callback($current, $key, $iterator) {
    // Здесь ваш код фильтрации
}

?>
```

Фільтрація рекурсивного ітератора зазвичай включає дві умови. Перше у тому, щоб дозволити рекурсію. Callback-функція має повертати \*\*`true`\*\*якщо поточний елемент ітератора має нащадків. Друге - це нормальна умова фільтра, наприклад, перевірка розміру файлу чи розширення, як у наведеному нижче прикладі.

**Приклад #2 Простий приклад рекурсивного зворотного виклику**

```php
<?php

$dir = new RecursiveDirectoryIterator(__DIR__);

// Фильтр больших файлов ( > 100MB)
$files = new RecursiveCallbackFilterIterator($dir, function ($current, $key, $iterator) {
    // Разрешить рекурсию
    if ($iterator->hasChildren()) {
        return TRUE;
    }
    // Проверка больших файлов
    if ($current->isFile() && $current->getSize() > 104857600) {
        return TRUE;
    }
    return FALSE;
});

foreach (new RecursiveIteratorIterator($files) as $file) {
    echo $file->getPathname() . PHP_EOL;
}

?>
```

## Зміст

-   [RecursiveCallbackFilterIterator::\_\_construct](recursivecallbackfilteriterator.construct.md)— Створює об'єкт класу RecursiveCallbackFilterIterator на основі об'єкта RecursiveIterator
-   [RecursiveCallbackFilterIterator::getChildren](recursivecallbackfilteriterator.getchildren.md)— Повертає дочірні елементи ітератора, що зберігається всередині RecursiveCallbackFilterIterator
-   [RecursiveCallbackFilterIterator::hasChildren](recursivecallbackfilteriterator.haschildren.md)— Перевіряє, чи поточний елемент внутрішнього ітератора містить дочірні елементи.
