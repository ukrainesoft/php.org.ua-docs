Обчислює розбіжність масивів, використовуючи callback-функцію порівняння ключів

-   [« arraydiffuassoc](function.array-diff-uassoc.html)
    
-   [arraydiff »](function.array-diff.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з масивами](ref.array.html)
    
-   Обчислює розбіжність масивів, використовуючи callback-функцію порівняння ключів
    

# arraydiffukey

(PHP 5> = 5.1.0, PHP 7, PHP 8)

arraydiffukey - обчислює розбіжність масивів, використовуючи callback-функцію для порівняння ключів

### Опис

```methodsynopsis
array_diff_ukey(array $array, array ...$arrays, callable $key_compare_func): array
```

Порівнює ключі `array` з ключами `arrays` та повертає різницю. Ця функція схожа на [arraydiff()](function.array-diff.html) крім того, що порівнюються ключі, а чи не значення.

На відміну від функції [arraydiffkey()](function.array-diff-key.html) для порівняння ключів використовується функція, що надається користувачем, а не вбудована функція.

### Список параметрів

`array`

Вихідний масив

`arrays`

Масиви, з якими йде порівняння

`key_compare_func`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

### Значення, що повертаються

Повертає масив (array), що містить усі елементи `array`, відсутні у якомусь із інших масивів.

### Приклади

**Приклад #1 Приклад використання **arraydiffukey()****

```php
<?php
function key_compare_func($key1, $key2)
{
    if ($key1 == $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_diff_ukey($array1, $array2, 'key_compare_func'));
?>
```

Результат виконання цього прикладу:

```
array(2) {
  ["red"]=>
  int(2)
  ["purple"]=>
  int(4)
}
```

### Примітки

> **Зауваження**
> 
> Зверніть увагу, що ця функція обробляє лише один вимір n-розмірного масиву. Звичайно, ви можете обробляти і більш глибокі рівні вкладеності, наприклад, використовуючи `array_diff_ukey($array1[0], $array2[0], 'callback_func');`

### Дивіться також

-   [arraydiff()](function.array-diff.html) - Обчислити розбіжність масивів
-   [arrayudiff()](function.array-udiff.html) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [arraydiffassoc()](function.array-diff-assoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [arraydiffuassoc()](function.array-diff-uassoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayudiffassoc()](function.array-udiff-assoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [arrayudiffuassoc()](function.array-udiff-uassoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [arraydiffkey()](function.array-diff-key.html) - обчислює розбіжність масивів, порівнюючи ключі
-   [arrayintersect()](function.array-intersect.html) - обчислює сходження масивів
-   [arrayintersectassoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayintersectuassoc()](function.array-intersect-uassoc.html) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayintersectkey()](function.array-intersect-key.html) - Обчислити перетин масивів, порівнюючи ключі
-   [arrayintersectukey()](function.array-intersect-ukey.html) - обчислює сходження масивів, використовуючи callback-функцію для порівняння ключів