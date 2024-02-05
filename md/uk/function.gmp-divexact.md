---
navigation:
  - function.gmp-div.md: « gmp\_div
  - function.gmp-export.md: gmp\_export »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_divexact
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_divexact

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_divexact — ділить числа без залишку

### Опис

```methodsynopsis
gmp_divexact(GMP|int|string $num1, GMP|int|string $num2): GMP
```

ділить число `num1`на`num2`, використовуючи швидкий алгоритм поділу без залишку. Функція видає коректний результат, тільки якщо відомо, що число `num2` ділить `num1`нацело.

### Список параметрів

`num1`

Подільне.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Дільник числа `num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_divexact()\*\*\*\*

```php
<?php
$div1 = gmp_divexact("10", "2");
echo gmp_strval($div1) . "\n";

$div2 = gmp_divexact("10", "3"); // некорректный результат
echo gmp_strval($div2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
5
2863311534
```
