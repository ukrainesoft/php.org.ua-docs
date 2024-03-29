---
navigation:
  - function.uasort.md: « uasort
  - function.usort.md: usort »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: uksort
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uksort

(PHP 4, PHP 5, PHP 7, PHP 8)

uksort — Сортує масив за ключами користувальницькою функцією порівняння

### Опис

```methodsynopsis
uksort(array &$array, callable $callback): true
```

Сортує масив (`array`) за ключами користувальницькою функцією порівняння, в якій визначено порядок сортування.

> **Зауваження** :
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

> **Зауваження** :
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Список параметрів

`array`

Вхідний масив

`callback`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |
| 8.0.0 | Тепер функція видасть помилку рівня **`E_WARNING`**, якщо параметр callback-функції, переданої у параметр `callback`, очікує на передачу значення за посиланням. |

### Приклади

**Приклад #1 Приклад використання функції** uksort()\*\*\*\*

```php
<?php

function cmp($a, $b)
{
    $a = preg_replace('@^(a|an|the) @', '', $a);
    $b = preg_replace('@^(a|an|the) @', '', $b);
    return strcasecmp($a, $b);
}

$a = array("John" => 1, "the Earth" => 2, "an apple" => 3, "a banana" => 4);

uksort($a, "cmp");

foreach ($a as $key => $value) {
    echo "$key: $value\n";
}
?>
```

Результат виконання наведеного прикладу:

```
an apple: 3
a banana: 4
the Earth: 2
John: 1
```

### Дивіться також

-   [usort()](function.usort.md) \- Сортує масив за значеннями використовуючи функцію користувача для порівняння елементів
-   [uasort()](function.uasort.md) \- Сортує масив користувальницькою функцією порівняння, зберігаючи асоціацію індексів
-   [Порівняння функцій сортування масивів](array.sorting.md)
