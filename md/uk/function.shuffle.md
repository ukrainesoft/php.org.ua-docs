---
navigation:
  - function.rsort.md: « rsort
  - function.sizeof.md: sizeof »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: shuffle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shuffle

(PHP 4, PHP 5, PHP 7, PHP 8)

shuffle - Перемішує масив

### Опис

```methodsynopsis
shuffle(array &$array): true
```

Функція перемішує елементи масиву випадковому порядку.

**Застереження**

Функція не створює криптографічно захищені значення та *не повинна* використовуватися для криптографічних цілей або цілей, що вимагають, щоб значення, що повертаються, були недоступні для розгадування.

Якщо потрібна криптографічно безпечна випадкова послідовність, можна використати клас [Random\\Randomizer](class.random-randomizer.md) з двигуном [Random\\Engine\\Secure](class.random-engine-secure.md). Для простих сценаріїв є функції [random\_int()](function.random-int.md) і [random\_bytes()](function.random-bytes.md) із зручним API криптографічно безпечного генератора псевдовипадкових чисел (CSPRNG), що підтримується операційною системою.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Внутрішній алгоритм отримання випадкових чисел [змінено](migration71.incompatible.md#migration71.incompatible.rand-srand-aliases) з функції rand бібліотеки libc на генератор на базі [» Вихор Мерсена.](http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.md) |

### Приклади

**Пример #1 Пример использования**shuffle()\*\*\*\*

```php
<?php
$numbers = range(1, 20);
shuffle($numbers);
foreach ($numbers as $number) {
    echo "$number ";
}
?>
```

### Примітки

> **Зауваження**: Ця функція надає нові ключі елементам `array`. Вона видалить усі існуючі ключі, а не просто переупорядкує їх.

> **Зауваження** :
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Дивіться також

-   [Random\\Randomizer::shuffleArray()](random-randomizer.shufflearray.md) \- Отримує перестановку масиву
-   [Random\\Randomizer::shuffleBytes()](random-randomizer.shufflebytes.md) \- отримує байтову перестановку рядка
-   [Random\\Randomizer::pickArrayKeys()](random-randomizer.pickarraykeys.md) \- Вибирає випадкові ключі масиву
-   [Порівняння функцій сортування масивів](array.sorting.md)
