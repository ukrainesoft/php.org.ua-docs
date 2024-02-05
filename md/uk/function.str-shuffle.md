---
navigation:
  - function.str-rot13.md: « str\_rot13
  - function.str-split.md: str\_split »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: str\_shuffle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# str\_shuffle

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

str\_shuffle — Переставляє символи у рядку випадковим чином

### Опис

```methodsynopsis
str_shuffle(string $string): string
```

**str\_shuffle()** перемішує символи у рядку. Вибирається одна можлива перестановка із усіх можливих.

**Застереження**

Функція не створює криптографічно захищені значення та *не повинна* використовуватися для криптографічних цілей або цілей, що вимагають, щоб значення, що повертаються, були недоступні для розгадування.

Якщо потрібна криптографічно безпечна випадкова послідовність, можна використати клас [Random\\Randomizer](class.random-randomizer.md) з двигуном [Random\\Engine\\Secure](class.random-engine-secure.md). Для простих сценаріїв є функції [random\_int()](function.random-int.md) і [random\_bytes()](function.random-bytes.md) із зручним API криптографічно безпечного генератора псевдовипадкових чисел (CSPRNG), що підтримується операційною системою.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає перемішаний рядок.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Внутрішній алгоритм отримання випадкових чисел [змінено](migration71.incompatible.md#migration71.incompatible.rand-srand-aliases) з функції rand бібліотеки libc на генератор на базі [» Вихор Мерсена](http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.md) |

### Приклади

**Пример #1 Пример использования**str\_shuffle()\*\*\*\*

```php
<?php
$str = 'abcdef';
$shuffled = str_shuffle($str);

// выведет что-то вроде этого: bfdaec
echo $shuffled;
?>
```

### Дивіться також

-   [Random\\Randomizer::shuffleBytes()](random-randomizer.shufflebytes.md) \- отримує байтову перестановку рядка
-   [Random\\Randomizer::shuffleArray()](random-randomizer.shufflearray.md) \- Отримує перестановку масиву
