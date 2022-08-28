Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції

-   [« Ds\\Deque::count](ds-deque.count.html)
    
-   [Ds\\Deque::find »](ds-deque.find.html)
    
-   [PHP Manual](index.html)
    
-   [Двухсторонняя очередь](class.ds-deque.html)
    
-   Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції
    

# ДсDeque::filter

(PECL ds >= 1.0.0)

ДсDeque::filter — Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції

### Опис

```methodsynopsis
public Ds\Deque::filter(callable $callback = ?): Ds\Deque
```

Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): bool
```

Опціональний аргумент типу [callable](language.types.callable.html), який повертає **`true`**, якщо значення має бути включено та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`** (дивіться [приведение к boolean](language.types.boolean.html#language.types.boolean.casting)

### Значення, що повертаються

Нова двостороння черга, що містить значення, для яких функція `callback` повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback` не заданий.

### Приклади

**Приклад #1 Приклад **ДсDeque::filter()** з використанням callback-функції**

```php
<?php
$deque = new \Ds\Deque([1, 2, 3, 4, 5]);

var_dump($deque->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Deque)#3 (2) {
  [0]=>
  int(2)
  [1]=>
  int(4)
}
```

**Приклад #2 Приклад **ДсDeque::filter()** без callback-функції**

```php
<?php
$deque = new \Ds\Deque([0, 1, 'a', true, false]);

var_dump($deque->filter());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Deque)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  string(1) "a"
  [2]=>
  bool(true)
}
```