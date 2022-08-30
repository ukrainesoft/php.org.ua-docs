Вибирає ключ із масиву

-   [« keyexists](function.key-exists.html)
    
-   [krsort »](function.krsort.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з масивами](ref.array.html)
    
-   Вибирає ключ із масиву
    

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

Функція **key()** просто повертає ключ того елемента масиву, який в даний момент вказує внутрішній покажчик масиву. Вона не зрушує покажчик у жодному напрямку. Якщо внутрішній покажчик вказує поза межами масиву або масив порожній, **key()** поверне **`null`**

### список змін

| Версия | Описание                                                                                                                                                                                                                                     |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку використовуйте для об'єкта (object) функцію [getmangledobjectvars()](function.get-mangled-object-vars.html)або використовуйте [ArrayIterator](class.arrayiterator.html) |

### Приклади

**Приклад #1 Приклад використання **key()****

```php
<?php
$array = array(
    'fruit1' => 'apple',
    'fruit2' => 'orange',
    'fruit3' => 'grape',
    'fruit4' => 'apple',
    'fruit5' => 'apple');

// этот цикл выведет все ключи ассоциативного массива,
// значения которых равны "apple"
while ($fruit_name = current($array)) {
    if ($fruit_name == 'apple') {
        echo key($array), "\n";
    }
    next($array);
}
?>
```

Результат виконання цього прикладу:

```
fruit1
fruit4
fruit5
```

### Дивіться також

-   [current()](function.current.html) - Повертає поточний елемент масиву
-   [next()](function.next.html) - Переміщує покажчик масиву вперед на один елемент
-   [arraykeyfirst()](function.array-key-first.html) - Отримує перший ключ масиву
-   [foreach](control-structures.foreach.html)