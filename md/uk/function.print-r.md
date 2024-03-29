---
navigation:
  - function.isset.md: « isset
  - function.serialize.md: serialize »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: print\_r
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# print\_r

(PHP 4, PHP 5, PHP 7, PHP 8)

print\_r — Виводить інформацію, що читає легко, про змінну

### Опис

```methodsynopsis
print_r(mixed $value, bool $return = false): string|bool
```

Функция**print\_r()** виводить інформацію про змінну у легкочитаному вигляді.

Функциям**print\_r()** [var\_dump()](function.var-dump.md) і [var\_export()](function.var-export.md) дозволено також показувати захищені та закриті атрибути об'єктів. Статичні елементи класу не відображатимуться.

### Список параметрів

`value`

Вираз для виведення на екран.

`return`

Якщо потрібно перехопити виведення функції **print\_r()**, необходимо задать параметр`return`. Якщо для цього параметра встановлено значення **`true`**, то функция**print\_r()** поверне інформацію, а чи не виведе її.

### Значення, що повертаються

Якщо в функцію передано рядок (string), ціле число (int) або число з плаваючою точкою (float), буде надруковано саме значення. Якщо передано масив (array), значення будуть надруковані у форматі, що показує ключі та елементи масиву. Аналогічний формат виводу буде застосовано для об'єктів.

Якщо параметр `return`установлен в\*\*`true`\*\*, функція поверне рядок (string). В іншому випадку значення, що повертається, буде одно **`true`**

### Приклади

**Приклад #1 Приклад використання функції** print\_r()\*\*\*\*

```php
<pre>
<?php

$a = array ('a' => 'яблоко', 'b' => 'банан', 'c' => array ('x', 'y', 'z'));
print_r ($a);
?>
</pre>
```

Результат виконання наведеного прикладу:

```
<pre>
Array
(
    [a] => яблоко
    [b] => банан
    [c] => Array
        (
            [0] => x
            [1] => y
            [2] => z
        )
)
</pre>
```

**Приклад #2 Приклад использования параметра`return`**

```php
<?php
$b = array ('m' => 'обезьяна', 'foo' => 'bar', 'x' => array ('x', 'y', 'z'));
$results = print_r($b, true); // Переменная $results теперь содержит вывод print_r
?>
```

### Примітки

> **Зауваження** :
> 
> Оскільки в сигнатурі функції є параметр `return`, вона буде використовувати внутрішню буферизацію виведення до PHP 7.1.0, тому її не можна використовувати як callback-функцію при виклику функції [ob\_start()](function.ob-start.md)

### Дивіться також

-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
-   [var\_dump()](function.var-dump.md) \- Виводить інформацію про змінну
-   [var\_export()](function.var-export.md) \- Виводить або повертає інтерпретоване рядкове подання змінної
