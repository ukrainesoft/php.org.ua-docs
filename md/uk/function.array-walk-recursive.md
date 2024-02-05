---
navigation:
  - function.array-values.md: « array\_values
  - function.array-walk.md: array\_walk »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_walk\_recursive
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_walk\_recursive

(PHP 5, PHP 7, PHP 8)

array\_walk\_recursive — Рекурсивно застосовує функцію користувача до кожного елементу масиву

### Опис

```methodsynopsis
array_walk_recursive(array|object &$array, callable $callback, mixed $arg = null): bool
```

Застосовує функцію користувача `callback` до кожного елементу масиву `array`. Функція обробляє кожен елемент багатовимірного масиву.

### Список параметрів

`array`

Вхідний масив

`callback`

Зазвичай, `callback` приймає два параметри. Першим параметром є значення елемента масиву `array`, а другим - його ключ.

> **Зауваження** :
> 
> Якщо потрібно, щоб функція `callback` змінила значення у масиві, визначте перший параметр `callback` як [посилання](language.references.md). Тоді всі зміни будуть застосовані до елементів масиву.

`arg`

Якщо вказано необов'язковий параметр `arg`, то він буде переданий третім параметром функції `callback`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**array\_walk\_recursive()\*\*\*\*

```php
<?php
$sweet = array('a' => 'apple', 'b' => 'banana');
$fruits = array('sweet' => $sweet, 'sour' => 'lemon');

function test_print($item, $key)
{
    echo "$key содержит $item\n";
}

array_walk_recursive($fruits, 'test_print');
?>
```

Результат виконання наведеного прикладу:

```
a содержит apple
b содержит banana
sour содержит lemon
```

Зверніть увагу, що ключ '`sweet`' ніколи не відображається. Будь-який ключ, що містить значення типу array, не передаватиметься у функцію.

### Дивіться також

-   [array\_walk()](function.array-walk.md) \- Застосовує задану користувачем функцію кожного елемента масиву
