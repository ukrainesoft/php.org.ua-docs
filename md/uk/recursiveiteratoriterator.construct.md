---
navigation:
  - recursiveiteratoriterator.callhaschildren.md: '« RecursiveIteratorIterator::callHasChildren'
  - recursiveiteratoriterator.current.md: 'RecursiveIteratorIterator::current »'
  - index.md: PHP Manual
  - class.recursiveiteratoriterator.md: RecursiveIteratorIterator
title: 'RecursiveIteratorIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveIteratorIterator::\_\_construct

(PHP 5 >= 5.1.3, PHP 7, PHP 8)

RecursiveIteratorIterator::\_\_construct — Конструктор класу RecursiveIteratorIterator

### Опис

public **RecursiveIteratorIterator::\_\_construct** [Traversable](class.traversable.md) `$iterator`, int`$mode`\= RecursiveIteratorIterator::LEAVES\_ONLY, int`$flags`

Створює новий об'єкт класу [RecursiveIteratorIterator](class.recursiveiteratoriterator.md) на основі об'єкта [RecursiveIterator](class.recursiveiterator.md)

### Список параметрів

`iterator`

Об'єкт-ітератор, на основі якого потрібно побудувати цей екземпляр. Це може бути об'єкт класу [RecursiveIterator](class.recursiveiterator.md)или класса[IteratorAggregate](class.iteratoraggregate.md)

`mode`

Необов'язковий параметр. Завдання режиму роботи архітектора. Можливі значення:

-   \*\*`RecursiveIteratorIterator::LEAVES_ONLY`\*\*- За замовчуванням. Ітерація здійснюватиметься лише з листів дерева елементів.
-   \*\*`RecursiveIteratorIterator::SELF_FIRST`\*\*- Ітерація здійснюватиметься по всьому дереву елементів, причому першими будуть батьківські елементи.
-   \*\*`RecursiveIteratorIterator::CHILD_FIRST`\*\*- Ітерація буде здійснюватись по всьому дереву елементів, причому першими будуть йти дочірні елементи.

`flags`

Необов'язковий прапор. Можливе значення **`RecursiveIteratorIterator::CATCH_GET_CHILD`** дає розпорядження об'єкту не брати до уваги винятки, які викликає метод **RecursiveIteratorIterator::getChildren()**

### Приклади

**Приклад #1 Ітерація з дерева елементів за допомогою RecursiveIteratorIterator**

```php
<?php
$array = array(
    array(
        array(
            array(
                'leaf-0-0-0-0',
                'leaf-0-0-0-1'
            ),
            'leaf-0-0-0'
        ),
        array(
            array(
                'leaf-0-1-0-0',
                'leaf-0-1-0-1'
            ),
            'leaf-0-1-0'
        ),
        'leaf-0-0'
    )
);

$iterator = new RecursiveIteratorIterator(
    new RecursiveArrayIterator($array),
    $mode
);
foreach ($iterator as $key => $leaf) {
    echo "$key => $leaf", PHP_EOL;
}
?>
```

Виведення прикладу в режимі `$mode = RecursiveIteratorIterator::LEAVES_ONLY`

```
0 => leaf-0-0-0-0
1 => leaf-0-0-0-1
0 => leaf-0-0-0
0 => leaf-0-1-0-0
1 => leaf-0-1-0-1
0 => leaf-0-1-0
0 => leaf-0-0
```

Виведення прикладу в режимі `$mode = RecursiveIteratorIterator::SELF_FIRST`

```
0 => Array
0 => Array
0 => Array
0 => leaf-0-0-0-0
1 => leaf-0-0-0-1
1 => leaf-0-0-0
1 => Array
0 => Array
0 => leaf-0-1-0-0
1 => leaf-0-1-0-1
1 => leaf-0-1-0
2 => leaf-0-0
```

Виведення прикладу в режимі `$mode = RecursiveIteratorIterator::CHILD_FIRST`

```
0 => leaf-0-0-0-0
1 => leaf-0-0-0-1
0 => Array
1 => leaf-0-0-0
0 => Array
0 => leaf-0-1-0-0
1 => leaf-0-1-0-1
0 => Array
1 => leaf-0-1-0
1 => Array
2 => leaf-0-0
0 => Array
```
