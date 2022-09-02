---
navigation:
  - function.mt-getrandmax.md: « mtgetrandmax
  - function.mt-srand.md: мтsrand »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: мтrand
---
# мтrand

(PHP 4, PHP 5, PHP 7, PHP 8)

мтrand - Генерує випадкове значення методом за допомогою генератора простих чисел на базі Вихря Мерсенна

### Опис

```methodsynopsis
mt_rand(): int
```

```methodsynopsis
mt_rand(int $min, int $max): int
```

**Застереження**

Ця функція не генерує криптографічно безпечні значення і не повинна використовуватись у криптографічних цілях. Якщо вам потрібне криптографічно безпечне значення, подумайте про використання функцій [randomint()](function.random-int.md) [randombytes()](function.random-bytes.md) або [opensslrandompseudobytes()](function.openssl-random-pseudo-bytes.md) замість цієї.

Багато генераторів випадкових чисел у старих бібліотеках мають сумнівні чи невідомі характеристики, а також працюють досить повільно. Функція **мтrand()** є заміною старої функції [rand()](function.rand.md). Вона використовує генератор випадкових чисел з відомими характеристиками, заснований на [» Вихор Мерсенна](http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.md)що генерує випадкові числа в середньому в чотири рази швидше, ніж libc rand().

Викликана без необов'язкових параметрів `min` і `max`, функція **мтrand()** повертає псевдовипадкове значення між 0 та [мтgetrandmax()](function.mt-getrandmax.md). Якщо потрібно, наприклад, випадкове число між 5 і 15 (включно), використовуйте виклик `mt_rand(5,15)`

### Список параметрів

`min`

Необов'язковий параметр: мінімальне значення випадкового числа (за замовчуванням: 0)

`max`

Необов'язковий параметр: максимальне значення випадкового числа (за замовчуванням: [мтgetrandmax()](function.mt-getrandmax.md)

### Значення, що повертаються

Випадкове ціле значення між `min` (або 0) та `max` (або [мтgetrandmax()](function.mt-getrandmax.md), включно), або **`false`** у разі якщо `max` менше `min`

### список змін

| Версия | Описание |
| --- | --- |
|  | Для **мтrand()** [произведено исправление бага](migration72.incompatible.md#migration72.incompatible.rand-mt_rand-output) усунення по модулю. Це означає, що послідовності згенеровані з конкретним початковим значенням можуть відрізнятися від згенерованих PHP 7.1 для 64-бітних машин. |
|  | [rand()](function.rand.md) [тепер є](migration71.incompatible.md#migration71.incompatible.rand-srand-aliases) псевдонімом для **мтrand()** |
|  | Функція **мтrand()** [була оновлена](migration71.incompatible.md#migration71.incompatible.fixes-to-mt_rand-algorithm) і тепер використовує коректну версію генератора випадкових чисел з урахуванням Вихря Мерсенна. Для використання старої поведінки, використовуйте [мтsrand()](function.mt-srand.md) з другим параметром, встановленим у **`MT_RAND_PHP`** |

### Приклади

**Приклад #1 Приклад використання **мтrand()****

```php
<?php
echo mt_rand() . "\n";
echo mt_rand() . "\n";

echo mt_rand(5, 15);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
1604716014
1478613278
6
```

### Примітки

**Увага**

Діапазон `min` `max` не повинен виходити за кордон [мтgetrandmax()](function.mt-getrandmax.md). Тобто (`max` `min`) <= [мтgetrandmax()](function.mt-getrandmax.md). В іншому випадку, **мтrand()** може повертати менш якісні випадкові числа.

### Дивіться також

-   [мтsrand()](function.mt-srand.md) - Проініціалізує генератор випадкових чисел на базі Вихря Мерсенна
-   [мтgetrandmax()](function.mt-getrandmax.md) - Показує максимально можливе значення випадкового числа
-   [randomint()](function.random-int.md) - Генерує криптографічно безпечні псевдовипадкові цілі числа
-   [randombytes()](function.random-bytes.md) - Генерує криптографічно безпечні псевдовипадкові байти
-   [opensslrandompseudobytes()](function.openssl-random-pseudo-bytes.md) - Генерує псевдовипадкову послідовність байт
-   [rand()](function.rand.md) - Генерує випадкове число
