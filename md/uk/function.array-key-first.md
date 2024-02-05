---
navigation:
  - function.array-key-exists.md: « array\_key\_exists
  - function.array-key-last.md: array\_key\_last »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_key\_first
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_key\_first

(PHP 7 >= 7.3.0, PHP 8)

array\_key\_first — Отримує перший ключ масиву

### Опис

```methodsynopsis
array_key_first(array $array): int|string|null
```

Отримати перший ключ заданого масиву `array`, не торкаючись внутрішнього покажчика масиву.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає перший ключ масиву `array`якщо він не порожній; **`null`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** array\_key\_first()\*\*\*\*

```php
<?php
$array = ['a' => 1, 'b' => 2, 'c' => 3];

$firstKey = array_key_first($array);

var_dump($firstKey);
?>
```

Результат виконання наведеного прикладу:

```
string(1) "a"
```

### Примітки

**Підказка**

Є кілька способів надати функціональність для версій PHP 7.3.0. Можна використовувати [array\_keys()](function.array-keys.md)Але це може бути досить неефективним. Також можна використовувати [reset()](function.reset.md) і [key()](function.key.md)але це може змінити внутрішній покажчик масиву. Ефективне рішення, яке не змінює внутрішній покажчик масиву, записаний як поліфіл:

```php
<?php
if (!function_exists('array_key_first')) {
    function array_key_first(array $arr) {
        foreach($arr as $key => $unused) {
            return $key;
        }
        return NULL;
    }
}
?>
```

### Дивіться також

-   [array\_key\_last()](function.array-key-last.md) \- Отримує останній ключ масиву
-   [reset()](function.reset.md) - Встановлює внутрішній покажчик масиву на перший елемент
