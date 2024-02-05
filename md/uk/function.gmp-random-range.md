---
navigation:
  - function.gmp-random-bits.md: « gmp\_random\_bits
  - function.gmp-random-seed.md: gmp\_random\_seed »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_random\_range
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_random\_range

(PHP 5 >= 5.6.3, PHP 7, PHP 8)

gmp\_random\_range — Отримує рівномірно вибране ціле число

### Опис

```methodsynopsis
gmp_random_range(GMP|int|string $min, GMP|int|string $max): GMP
```

Генерує довільне число. Число буде в діапазоні між значеннями параметрів `min`и`max`

Обидва числа у параметрах `min`и`max` можуть бути негативними, але число `min` має бути менше числа `max`

**Застереження**

Функція не створює криптографічно захищені значення та *не повинна* використовуватися для криптографічних цілей або цілей, що вимагають, щоб значення, що повертаються, були недоступні для розгадування.

Якщо потрібна криптографічно безпечна випадкова послідовність, можна використати клас [Random\\Randomizer](class.random-randomizer.md) з двигуном [Random\\Engine\\Secure](class.random-engine-secure.md). Для простих сценаріїв є функції [random\_int()](function.random-int.md) і [random\_bytes()](function.random-bytes.md) із зручним API криптографічно безпечного генератора псевдовипадкових чисел (CSPRNG), що підтримується операційною системою.

### Список параметрів

`min`

GMP-число - нижня межа випадкового числа.

`max`

GMP-число - верхня межа випадкового числа.

### Значення, що повертаються

Повертає об'єкт [GMP](class.gmp.md), який містить рівномірно вибране ціле число з інтервалу \[`min` `max`\]Значения параметров`min`и`max` можуть виявитися значеннями, що повертаються.

### Помилки

Якщо число у параметрі `max`окажется меньше числа в параметре`min`, буде викинуто виняток [ValueError](class.valueerror.md)

### Приклади

**Пример #1 Пример использования функции**gmp\_random\_range()\*\*\*\*

```php
<?php
$rand1 = gmp_random_range(0, 100);    // случайное число между 0 и 100
$rand2 = gmp_random_range(-100, -10); // случайное число между -100 и -10

echo gmp_strval($rand1) . "\n";
echo gmp_strval($rand2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
42
-67
```
