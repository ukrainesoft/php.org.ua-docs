---
navigation:
  - function.lcg-value.md: « lcg\_value
  - function.mt-rand.md: mt\_rand »
  - index.md: PHP Manual
  - ref.random.md: Функції Random
title: mt\_getrandmax
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mt\_getrandmax

(PHP 4, PHP 5, PHP 7, PHP 8)

mt\_getrandmax — Вказує максимально можливе значення випадкового числа

### Опис

```methodsynopsis
mt_getrandmax(): int
```

Повертає максимальне значення, яке можна отримати при виклику [mt\_rand()](function.mt-rand.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає максимальне випадкове значення, що повертається [mt\_rand()](function.mt-rand.md), викликаного без аргументів, тобто максимальне значення, яке можна передати до параметра `max`так щоб результат не округлився і, відповідно, не зменшувалася випадковість.

### Дивіться також

-   [mt\_rand()](function.mt-rand.md) \- Генерує випадкове значення методом за допомогою генератора простих чисел на базі Вихря Мерсенна
-   [mt\_srand()](function.mt-srand.md) \- Ініціалізує генератор випадкових чисел на базі Вихря Мерсенна
-   [getrandmax()](function.getrandmax.md) \- Повертає максимально можливе випадкове число
