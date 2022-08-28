Повертає поточний елемент масиву

-   [« count](function.count.html)
    
-   [each »](function.each.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Повертає поточний елемент масиву
    

# current

(PHP 4, PHP 5, PHP 7, PHP 8)

current — Повертає поточний елемент масиву

### Опис

```methodsynopsis
current(array|object $array): mixed
```

У кожного масиву є внутрішній покажчик з його " поточний " елемент, який ініціалізується першим елементом, доданим масив.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Функція **current()** просто повертає значення елемента масиву, який вказує його внутрішній покажчик. Вона не переміщає покажчик будь-куди. Якщо внутрішній покажчик знаходиться за межами списку елементів або масив порожній, **current()** повертає **`false`**

**Увага**

Ця функція може повертати як логічне значення **`false`**так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Описание |
| --- | --- |
|  | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку використовуйте для об'єкта (object) функцію [get\_mangled\_object\_vars()](function.get-mangled-object-vars.html)або використовуйте [ArrayIterator](class.arrayiterator.html) |

### Приклади

**Приклад #1 Приклад використання **current()** та дружніх функцій**

```php
<?php
$transport = array('foot', 'bike', 'car', 'plane');
$mode = current($transport); // $mode = 'foot';
$mode = next($transport);    // $mode = 'bike';
$mode = current($transport); // $mode = 'bike';
$mode = prev($transport);    // $mode = 'foot';
$mode = end($transport);     // $mode = 'plane';
$mode = current($transport); // $mode = 'plane';

$arr = array();
var_dump(current($arr)); // bool(false)

$arr = array(array());
var_dump(current($arr)); // array(0) { }
?>
```

### Примітки

> **Зауваження**: Результати виклику **current()** на порожньому масиві та на масиві, внутрішній покажчик якого вказує на кінець елементів, не відрізняються від елемента масиву типу bool зі значенням **`false`**. Для коректного обходу масиву, який може містити **`false`**дивіться керуючу конструкцію [foreach](control-structures.foreach.html). Якщо ви хочете використовувати функцію **current()** та при цьому коректно відстежувати кінець масиву, використовуйте функцію [key()](function.key.html) на тому ж елементі, на якому використовували **current()** і перевіряйте її результат на сувору нерівність **`null`**

### Дивіться також

-   [end()](function.end.html) - Встановлює внутрішній покажчик масиву на його останній елемент
-   [key()](function.key.html) - Вибирає ключ із масиву
-   [each()](function.each.html) - Повертає поточну пару ключ/значення з масиву та зміщує його покажчик
-   [prev()](function.prev.html) - Пересуває внутрішній покажчик масиву на одну позицію назад
-   [reset()](function.reset.html) - Встановлює внутрішній покажчик масиву на його перший елемент
-   [next()](function.next.html) - Переміщує покажчик масиву вперед на один елемент
-   [foreach](control-structures.foreach.html)