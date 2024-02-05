---
navigation:
  - function.mt-srand.md: « mt\_srand
  - function.random-bytes.md: random\_bytes »
  - index.md: PHP Manual
  - ref.random.md: Функції Random
title: rand
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rand

(PHP 4, PHP 5, PHP 7, PHP 8)

rand - Генерує випадкове число

### Опис

```methodsynopsis
rand(): int
```

```methodsynopsis
rand(int $min, int $max): int
```

При дзвінку без параметрів `min`и`max`, возвращает псевдослучайное целое в диапазоне от 0 до[getrandmax()](function.getrandmax.md). Наприклад, якщо вам потрібне випадкове число між 5 і 15 (включно), викличте `rand(5, 15)`

**Застереження**

Функція не створює криптографічно захищені значення та *не повинна* використовуватися для криптографічних цілей або цілей, що вимагають, щоб значення, що повертаються, були недоступні для розгадування.

Якщо потрібна криптографічно безпечна випадкова послідовність, можна використати клас [Random\\Randomizer](class.random-randomizer.md) з двигуном [Random\\Engine\\Secure](class.random-engine-secure.md). Для простих сценаріїв є функції [random\_int()](function.random-int.md) і [random\_bytes()](function.random-bytes.md) із зручним API криптографічно безпечного генератора псевдовипадкових чисел (CSPRNG), що підтримується операційною системою.

> **Зауваження**: На деяких платформах (таких як Windows) [getrandmax()](function.getrandmax.md) лише 32767. Щоб розширити діапазон, використовуйте параметри `min`и`max`, або зверніться до функції [mt\_rand()](function.mt-rand.md)

> **Зауваження**: Починаючи з PHP 7.1.0, **rand()** використовує той же алгоритм отримання випадкових чисел, що й [mt\_rand()](function.mt-rand.md). Для збереження зворотної сумісності, функція **rand()** дозволяє задавати параметр `max`меньше, чем параметр`min`Функция[mt\_rand()](function.mt-rand.md) у такій ситуації повертатиме **`false`**

### Список параметрів

`min`

Найменше значення, яке можна повернути (за замовчуванням: 0)

`max`

Найбільше значення, яке можна повернути (за замовчуванням: [getrandmax()](function.getrandmax.md)) .

### Значення, що повертаються

Псевдослучайное значение в диапазоне от`min`(или 0) до`max`(или[getrandmax()](function.getrandmax.md)

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Для**rand()** [здійснено виправлення бага](migration72.incompatible.md#migration72.incompatible.rand-mt_rand-output) усунення по модулю. Це означає, що послідовності згенеровані з конкретним початковим значенням можуть відрізнятися від згенерованих PHP 7.1 для 64-бітних машин. |
| 7.1.0 | [**rand()** стала синонімом функції](migration71.incompatible.md#migration71.incompatible.rand-srand-aliases) [mt\_rand()](function.mt-rand.md) |

### Приклади

**Приклад #1 Приклад використання** rand()\*\*\*\*

```php
<?php
echo rand(), "\n";
echo rand(), "\n";

echo rand(5, 15), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
7771
22264
11
```

### Примітки

**Увага**

Диапазон`min` `max` не повинен виходити за кордон [getrandmax()](function.getrandmax.md). Тобто (`max` `min`) <= [getrandmax()](function.getrandmax.md). В іншому випадку, **rand()** може повертати менш якісні довільні числа.

### Дивіться також

-   [srand()](function.srand.md) \- Задає початкове число генератора псевдовипадкових чисел
-   [getrandmax()](function.getrandmax.md) \- Повертає максимально можливе випадкове число
-   [mt\_rand()](function.mt-rand.md) \- Генерує випадкове значення методом за допомогою генератора простих чисел на базі Вихря Мерсенна
-   [random\_int()](function.random-int.md) \- Отримує криптографічно безпечне, рівномірно вибране ціле число
-   [random\_bytes()](function.random-bytes.md) \- Отримує криптографічно безпечні випадкові байти
