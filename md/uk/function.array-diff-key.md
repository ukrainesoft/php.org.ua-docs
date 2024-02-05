---
navigation:
  - function.array-diff-assoc.md: « array\_diff\_assoc
  - function.array-diff-uassoc.md: array\_diff\_uassoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_diff\_key
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_diff\_key

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

array\_diff\_key — обчислює розбіжність масивів, порівнюючи ключі

### Опис

```methodsynopsis
array_diff_key(array $array, array ...$arrays): array
```

Сравнивает ключи`array` з ключами `arrays` та повертає різницю. Ця функція схожа з [array\_diff()](function.array-diff.md) крім того, що порівнюються ключі, а чи не значення.

### Список параметрів

`array`

Вихідний масив

`arrays`

Масиви для порівняння

### Значення, що повертаються

Повертає масив (array), що містить усі елементи `array` з ключами, яких немає у всіх наступних масивах.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер функцію можна викликати лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання** array\_diff\_key()\*\*\*\*

Два ключа пар`key => value` вважаються рівними тільки тоді, коли `(string) $key1 === (string) $key2` . Іншими словами, застосовується сувора перевірка, що означає, що рядкові уявлення повинні бути однаковими.

```php
<?php
$array1 = array('blue' => 1, 'red' => 2, 'green' => 3, 'purple' => 4);
$array2 = array('green' => 5, 'yellow' => 7, 'cyan' => 8);

var_dump(array_diff_key($array1, $array2));
?>
```

Результат виконання наведеного прикладу:

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
$array1 = array('blue' => 1, 'red'  => 2, 'green' => 3, 'purple' => 4);
$array2 = array('green' => 5, 'yellow' => 7, 'cyan' => 8);
$array3 = array('blue' => 6, 'yellow' => 7, 'mauve' => 8);

var_dump(array_diff_key($array1, $array2, $array3));
?>
```

Результат виконання наведеного прикладу:

```
array(2) {
  ["red"]=>
  int(2)
  ["purple"]=>
  int(4)
}
```

### Примітки

> **Зауваження** :
> 
> Ця функція обробляє лише один вимір n-розмірного масиву. Звичайно, ви можете обробляти і більш глибокі рівні вкладеності, наприклад, використовуючи `array_diff_key($array1[0], $array2[0]);`

### Дивіться також

-   [array\_diff()](function.array-diff.md) \- обчислює розбіжність масивів
-   [array\_udiff()](function.array-udiff.md) \- обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_diff\_uassoc()](function.array-diff-uassoc.md) \- Обчислює розбіжність масивів з додатковою перевіркою індексу через пользовательскую callback-функцію
-   [array\_udiff\_assoc()](function.array-udiff-assoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [array\_udiff\_uassoc()](function.array-udiff-uassoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_diff\_ukey()](function.array-diff-ukey.md) \- обчислює розбіжність масивів, використовуючи callback-функцію для порівняння ключів
-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_intersect\_uassoc()](function.array-intersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, порівнюючи індекси через callback-функцію
-   [array\_intersect\_key()](function.array-intersect-key.md) \- обчислює перетин масивів, порівнюючи ключі
-   [array\_intersect\_ukey()](function.array-intersect-ukey.md) \- обчислює перетин масивів, використовуючи callback-функцію для порівняння ключів
