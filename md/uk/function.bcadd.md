---
navigation:
  - ref.bc.md: « Функції BC Math
  - function.bccomp.md: bccomp »
  - index.md: PHP Manual
  - ref.bc.md: Функції BC Math
title: bcadd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bcadd

(PHP 4, PHP 5, PHP 7, PHP 8)

bcadd — Скласти 2 числа довільної точності

### Опис

```methodsynopsis
bcadd(string $num1, string $num2, ?int $scale = null): string
```

Складає `num1`с`num2`

### Список параметрів

`num1`

Лівий операнд (доданок) у вигляді рядка.

`num2`

Правий операнд (доданок) у вигляді рядка.

`scale`

Цей необов'язковий параметр використовують для налаштування кількості знаків після десяткового роздільника в результаті. Якщо не задано, то, за замовчуванням, буде використано значення, задане глобально за допомогою [bcscale()](function.bcscale.md), либо

### Значення, що повертаються

Сума доданків у вигляді рядка.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `scale` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** bcadd()\*\*\*\*

```php
<?php

$a = '1.234';
$b = '5';

echo bcadd($a, $b);     // 6
echo bcadd($a, $b, 4);  // 6.2340

?>
```

### Дивіться також

-   [bcsub()](function.bcsub.md) \- Віднімає одне число з іншого із заданою точністю
