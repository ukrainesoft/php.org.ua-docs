---
navigation:
  - function.array-push.md: « array\_push
  - function.array-reduce.md: array\_reduce »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_rand
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_rand

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_rand - Вибирає один або кілька випадкових ключів з масиву

### Опис

```methodsynopsis
array_rand(array $array, int $num = 1): int|string|array
```

Вибирає одне чи кілька випадкових значень із масиву. Повертає ключ (або ключі) даних випадкових елементів.

**Застереження**

Функція не створює криптографічно захищені значення та *не повинна* використовуватися для криптографічних цілей або цілей, що вимагають, щоб значення, що повертаються, були недоступні для розгадування.

Якщо потрібна криптографічно безпечна випадкова послідовність, можна використати клас [Random\\Randomizer](class.random-randomizer.md) з двигуном [Random\\Engine\\Secure](class.random-engine-secure.md). Для простих сценаріїв є функції [random\_int()](function.random-int.md) і [random\_bytes()](function.random-bytes.md) із зручним API криптографічно безпечного генератора псевдовипадкових чисел (CSPRNG), що підтримується операційною системою.

### Список параметрів

`array`

Вхідний масив

`num`

Визначає кількість елементів, що вибираються.

### Значення, що повертаються

Якщо ви вибираєте лише одне значення, функція **array\_rand()** повертає ключ, який відповідає цьому значенню. У протилежному випадку вона повертає масив ключів, що відповідають випадковим значенням. Це зроблено для того, щоб дати можливість вибрати з масиву випадкові значення, так і випадкові ключі. Якщо повертається кілька ключів, вони будуть повернуті в порядку, в якому вони були присутні у вихідному масиві. Спроба вибрати більше елементів, ніж у масиві, згенерує помилку рівня **`E_WARNING`** та поверне NULL.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Внутрішній алгоритм отримання випадкових чисел [змінено](migration71.incompatible.md#migration71.incompatible.rand-srand-aliases) з функції rand бібліотеки libc на генератор на базі [» Вихор Мерсенна](http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.md) |

### Приклади

**Пример #1 Пример использования**array\_rand()\*\*\*\*

```php
<?php
$input = array("Neo", "Morpheus", "Trinity", "Cypher", "Tank");
$rand_keys = array_rand($input, 2);
echo $input[$rand_keys[0]] . "\n";
echo $input[$rand_keys[1]] . "\n";
?>
```

### Дивіться також

-   [Random\\Randomizer::pickArrayKeys()](random-randomizer.pickarraykeys.md) \- Вибирає випадкові ключі масиву
-   [Random\\Randomizer::shuffleArray()](random-randomizer.shufflearray.md) \- Отримує перестановку масиву
