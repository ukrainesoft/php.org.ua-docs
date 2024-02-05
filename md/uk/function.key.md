---
navigation:
  - function.key-exists.md: « key\_exists
  - function.krsort.md: krsort »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: key
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# key

(PHP 4, PHP 5, PHP 7, PHP 8)

key — Вибір ключа з масиву

### Опис

```methodsynopsis
key(array|object $array): int|string|null
```

**key()** повертає індекс поточного масиву елемента.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Функция**key()** просто повертає ключ того елемента масиву, який в даний момент вказує внутрішній покажчик масиву. Вона не зрушує покажчик у жодному напрямку. Якщо внутрішній покажчик вказує поза межами масиву або масив порожній, **key()**возвратит**`null`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку перетворіть об'єкт (object) на масив (array) за допомогою функції [get\_mangled\_object\_vars()](function.get-mangled-object-vars.md), або використовуйте методи, що надаються класом, що реалізує інтерфейс [Iterator](class.iterator.md), наПриклад,[ArrayIterator](class.arrayiterator.md) |
| 7.4.0 | Примірники класів [SPL](book.spl.md) тепер обробляються як порожні об'єкти, які мають властивостей, замість виклику методу [Iterator](class.iterator.md) з тим самим ім'ям, що і ця функція. |

### Приклади

**Приклад #1 Приклад використання** key()\*\*\*\*

```php
<?php
$array = array(
    'fruit1' => 'apple',
    'fruit2' => 'orange',
    'fruit3' => 'grape',
    'fruit4' => 'apple',
    'fruit5' => 'apple');

// этот цикл выведет все ключи ассоциативного массива,
// значения которых равны "apple"
while ($fruit_name = current($array)) {
    if ($fruit_name == 'apple') {
        echo key($array), "\n";
    }
    next($array);
}
?>
```

Результат виконання наведеного прикладу:

```
fruit1
fruit4
fruit5
```

### Дивіться також

-   [current()](function.current.md) \- Повертає поточний елемент масиву
-   [next()](function.next.md) \- Переміщує покажчик масиву вперед на один елемент
-   [array\_key\_first()](function.array-key-first.md) \- Отримує перший ключ масиву
-   [foreach](control-structures.foreach.md)
