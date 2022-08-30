Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції

-   [« DsVector::count](ds-vector.count.html)
    
-   [ДсVector::find »](ds-vector.find.html)
    
-   [PHP Manual](index.md)
    
-   [Вектор](class.ds-vector.html)
    
-   Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції
    

# ДсVector::filter

(PECL ds >= 1.0.0)

ДсVector::filter — Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції

### Опис

```methodsynopsis
public Ds\Vector::filter(callable $callback = ?): Ds\Vector
```

Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): bool
```

Опціональний аргумент типу [callable](language.types.callable.md), який повертає **`true`**, якщо значення має бути включено та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`** (дивіться [приведение к boolean](language.types.boolean.html#language.types.boolean.casting)

### Значення, що повертаються

Новий вектор, що містить значення, для яких функція `callback` повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback` не заданий.

### Приклади

**Приклад #1 Приклад **ДсVector::filter()** з використанням callback-функції**

```php
<?php
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

var_dump($vector->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Vector)#3 (2) {
  [0]=>
  int(2)
  [1]=>
  int(4)
}
```

**Приклад #2 Приклад **ДсVector::filter()** без callback-функції**

```php
<?php
$vector = new \Ds\Vector([0, 1, 'a', true, false]);

var_dump($vector->filter());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Vector)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  string(1) "a"
  [2]=>
  bool(true)
}
```