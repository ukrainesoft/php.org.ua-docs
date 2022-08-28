Обчислює розбіжність масивів, порівнюючи ключі

-   [« array\_diff\_assoc](function.array-diff-assoc.html)
    
-   [array\_diff\_uassoc »](function.array-diff-uassoc.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Обчислює розбіжність масивів, порівнюючи ключі
    

# arraydiffkey

(PHP 5> = 5.1.0, PHP 7, PHP 8)

arraydiffkey — обчислює розбіжність масивів, порівнюючи ключі

### Опис

```methodsynopsis
array_diff_key(array $array, array ...$arrays): array
```

Порівнює ключі `array` з ключами `arrays` та повертає різницю. Ця функція схожа з [array\_diff()](function.array-diff.html) крім того, що порівнюються ключі, а чи не значення.

### Список параметрів

`array`

Вихідний масив

`array`

Масиви для порівняння

### Значення, що повертаються

Повертає масив (array), що містить усі елементи `array` з ключами, яких немає у всіх наступних масивах.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання **arraydiffkey()****

Два ключі пар `key => value` вважаються рівними тільки тоді, коли `(string) $key1 === (string) $key2` . Іншими словами, застосовується сувора перевірка, що означає, що рядкові уявлення повинні бути однаковими.

```php
<?php
$array1 = array('blue' => 1, 'red' => 2, 'green' => 3, 'purple' => 4);
$array2 = array('green' => 5, 'yellow' => 7, 'cyan' => 8);

var_dump(array_diff_key($array1, $array2));
?>
```

Результат виконання цього прикладу:

```
array(3) {
  ["blue"]=>
  int(1)
  ["red"]=>
  int(2)
  ["purple"]=>
  int(4)
}
```

```php
<?php
$array1 = array('blue' => 1, 'red'  => 2, 'green' => 3, 'purple' => 4);
$array2 = array('green' => 5, 'yellow' => 7, 'cyan' => 8);
$array3 = array('blue' => 6, 'yellow' => 7, 'mauve' => 8);

var_dump(array_diff_key($array1, $array2, $array3));
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
> Ця функція обробляє лише один вимір n-розмірного масиву. Звичайно, ви можете обробляти і більш глибокі рівні вкладеності, наприклад, використовуючи `array_diff_key($array1[0], $array2[0]);`

### Дивіться також

-   [array\_diff()](function.array-diff.html) - Обчислити розбіжність масивів
-   [array\_udiff()](function.array-udiff.html) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_diff\_assoc()](function.array-diff-assoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_diff\_uassoc()](function.array-diff-uassoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [array\_udiff\_assoc()](function.array-udiff-assoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [array\_udiff\_uassoc()](function.array-udiff-uassoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_diff\_ukey()](function.array-diff-ukey.html) - обчислює розбіжність масивів, використовуючи callback-функцію для порівняння ключів
-   [array\_intersect()](function.array-intersect.html) - обчислює сходження масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [array\_intersect\_uassoc()](function.array-intersect-uassoc.html) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [array\_intersect\_key()](function.array-intersect-key.html) - Обчислити перетин масивів, порівнюючи ключі
-   [array\_intersect\_ukey()](function.array-intersect-ukey.html) - обчислює сходження масивів, використовуючи callback-функцію для порівняння ключів