---
navigation:
  - function.bcadd.md: « bcadd
  - function.bcdiv.md: bcdiv »
  - index.md: PHP Manual
  - ref.bc.md: Функції BC Math
title: bccomp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bccomp

(PHP 4, PHP 5, PHP 7, PHP 8)

bccomp — Порівняння двох чисел довільної точності

### Опис

```methodsynopsis
bccomp(string $num1, string $num2, ?int $scale = null): int
```

Сравнивает`num1`с`num2` і повертає цілий результат.

### Список параметрів

`num1`

Лівий операнд у вигляді рядка.

`num2`

Правий операнд у вигляді рядка.

`scale`

Необов'язковий аргумент `scale` задає кількість цифр після десяткової точки, яка братиме участь у порівнянні.

### Значення, що повертаються

Повертає 0, якщо числа дорівнюють; 1, якщо `left_operand`больше, чем`right_operand`; -1 якщо менше.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `scale` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**bccomp()\*\*\*\*

```php
<?php

echo bccomp('1', '2') . "\n";   // -1
echo bccomp('1.00001', '1', 3); // 0
echo bccomp('1.00001', '1', 5); // 1

?>
```
