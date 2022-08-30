Рекурсивно застосовує функцію користувача до кожного елементу масиву

-   [« arrayvalues](function.array-values.html)
    
-   [arraywalk »](function.array-walk.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з масивами](ref.array.html)
    
-   Рекурсивно застосовує функцію користувача до кожного елементу масиву
    

# arraywalkrecursive

(PHP 5, PHP 7, PHP 8)

arraywalkrecursive — Рекурсивно застосовує функцію користувача до кожного елементу масиву

### Опис

```methodsynopsis
array_walk_recursive(array|object &$array, callable $callback, mixed $arg = null): bool
```

Застосовує функцію користувача `callback` до кожного елементу масиву `input`. Ця функція обробляє кожен елемент багатовимірного масиву.

### Список параметрів

`array`

Вхідний масив

`callback`

Зазвичай, `callback` приймає два параметри. Першим параметром є значення елемента масиву `input`, а другим - його ключ.

> **Зауваження**
> 
> Якщо потрібно, щоб функція `callback` змінила значення у масиві, визначте перший параметр `callback` як [ссылку](language.references.html). Тоді всі зміни будуть застосовані до елементів масиву.

`arg`

Якщо вказано необов'язковий параметр `arg`, то він буде переданий третім параметром функції `callback`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **arraywalkrecursive()****

```php
<?php
$sweet = array('a' => 'apple', 'b' => 'banana');
$fruits = array('sweet' => $sweet, 'sour' => 'lemon');

function test_print($item, $key)
{
    echo "$key содержит $item\n";
}

array_walk_recursive($fruits, 'test_print');
?>
```

Результат виконання цього прикладу:

```
a содержит apple
b содержит banana
sour содержит lemon
```

Зверніть увагу, що ключ '`sweet`' ніколи не відображається. Будь-який ключ, що містить значення типу array, не передаватиметься у функцію.

### Дивіться також

-   [arraywalk()](function.array-walk.html) - Застосовує задану користувачем функцію кожного елемента масиву