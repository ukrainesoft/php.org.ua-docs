---
navigation:
  - function.array-unique.md: « array\_unique
  - function.array-values.md: array\_values »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_unshift
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_unshift

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_unshift — Додає один або кілька елементів на початок масиву

### Опис

```methodsynopsis
array_unshift(array &$array, mixed ...$values): int
```

**array\_unshift()** додає передані як аргументи елементи на початок масиву `array`. Зауважте, що список елементів додається повністю, тобто порядок елементів зберігається. Усі числові ключі будуть змінені таким чином, що нумерація масиву буде починатися з нуля, тоді як рядкові ключі залишаться незмінними.

> **Зауваження** :
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Список параметрів

`array`

Вхідний масив

`values`

Значення додавання.

### Значення, що повертаються

Повертає нову кількість елементів у `array`

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Тепер ця функція може бути викликана одним параметром. Раніше потрібно було мінімум два параметри. |

### Приклади

**Пример #1 Пример использования**array\_unshift()\*\*\*\*

```php
<?php
$queue = [
    "orange",
    "banana"
];

array_unshift($queue, "apple", "raspberry");
var_dump($queue);
?>
```

Результат виконання наведеного прикладу:

```
array(4) {
  [0] =>
  string(5) "apple"
  [1] =>
  string(9) "raspberry"
  [2] =>
  string(6) "orange"
  [3] =>
  string(6) "banana"
}
```

**Приклад #2 Приклад використання з асоціативними масивами**

Якщо один асоціативний масив додається до іншого асоціативного масиву, то масив, що додається, продовжує числовий індекс першого масиві.

```php
<?php
$foods = [
    'apples' => [
        'McIntosh' => 'red',
        'Granny Smith' => 'green',
    ],
    'oranges' => [
        'Navel' => 'orange',
        'Valencia' => 'orange',
    ],
];
$vegetables = [
    'lettuce' => [
        'Iceberg' => 'green',
        'Butterhead' => 'green',
    ],
    'carrots' => [
        'Deep Purple Hybrid' => 'purple',
        'Imperator' => 'orange',
    ],
    'cucumber' => [
        'Kirby' => 'green',
        'Gherkin' => 'green',
    ],
];

array_unshift($foods, $vegetables);
var_dump($foods);
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0] =>
  array(3) {
    'lettuce' =>
    array(2) {
      'Iceberg' =>
      string(5) "green"
      'Butterhead' =>
      string(5) "green"
    }
    'carrots' =>
    array(2) {
      'Deep Purple Hybrid' =>
      string(6) "purple"
      'Imperator' =>
      string(6) "orange"
    }
    'cucumber' =>
    array(2) {
      'Kirby' =>
      string(5) "green"
      'Gherkin' =>
      string(5) "green"
    }
  }
  'apples' =>
  array(2) {
    'McIntosh' =>
    string(3) "red"
    'Granny Smith' =>
    string(5) "green"
  }
  'oranges' =>
  array(2) {
    'Navel' =>
    string(6) "orange"
    'Valencia' =>
    string(6) "orange"
  }
}
```

### Дивіться також

-   [array\_shift()](function.array-shift.md) \- Витягує перший елемент масиву
-   [array\_push()](function.array-push.md) \- Додає один або кілька елементів у кінець масиву
-   [array\_pop()](function.array-pop.md) \- Витягує останній елемент масиву
