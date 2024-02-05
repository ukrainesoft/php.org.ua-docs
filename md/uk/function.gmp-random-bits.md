---
navigation:
  - function.gmp-prob-prime.md: « gmp\_prob\_prime
  - function.gmp-random-range.md: gmp\_random\_range »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_random\_bits
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_random\_bits

(PHP 5 >= 5.6.3, PHP 7, PHP 8)

gmp\_random\_bits - Генерує випадкове число

### Опис

```methodsynopsis
gmp_random_bits(int $bits): GMP
```

Генерирует случайное число. Число будет находиться в диапазоне между и`2$bits - 1`

Значение параметра`bits` має бути більше 0, а максимальне значення обмежено розміром доступної пам'яті.

**Застереження**

Функція не створює криптографічно захищені значення та *не повинна* використовуватися для криптографічних цілей або цілей, що вимагають, щоб значення, що повертаються, були недоступні для розгадування.

Якщо потрібна криптографічно безпечна випадкова послідовність, можна використати клас [Random\\Randomizer](class.random-randomizer.md) з двигуном [Random\\Engine\\Secure](class.random-engine-secure.md). Для простих сценаріїв є функції [random\_int()](function.random-int.md) і [random\_bytes()](function.random-bytes.md) із зручним API криптографічно безпечного генератора псевдовипадкових чисел (CSPRNG), що підтримується операційною системою.

### Список параметрів

`bits`

Кількість бітів для створення.

### Значення, що повертаються

Випадкове число GMP.

### Помилки

Если значение параметра`bits`будет меньше , буде викинуто виняток [ValueError](class.valueerror.md)

### Приклади

**Приклад #1 Приклад использования функции**gmp\_random\_bits()\*\*\*\*

```php
<?php

$rand1 = gmp_random_bits(3); // случайное число от 0 до 7
$rand2 = gmp_random_bits(5); // случайное число от 0 до 31

echo gmp_strval($rand1) . "\n";
echo gmp_strval($rand2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
3
15
```
