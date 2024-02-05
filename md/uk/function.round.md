---
navigation:
  - function.rad2deg.md: « rad2deg
  - function.sin.md: sin »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: round
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# round

(PHP 4, PHP 5, PHP 7, PHP 8)

round - Округлює число з плаваючою точкою (float)

### Опис

```methodsynopsis
round(int|float $num, int $precision = 0, int $mode = PHP_ROUND_HALF_UP): float
```

Повертає заокруглене значення числа `num` з точністю, вказаною у параметрі `precision` (кількість цифр після коми). Значення точності `precision` можна задавати негативним значенням або нулем (за замовчуванням).

### Список параметрів

`num`

Значення для заокруглення.

`precision`

Необов'язкова кількість десяткових знаків, до яких буде заокруглено число.

Якщо точність `precision` позитивна, число `num` округляється до точності `precision` значних цифр після десяткової точки.

Якщо точність `precision` негативна, число `num` округляється до точності `precision` значущих цифр перед десятковою точкою, тобто до наступного кратного результату виразу `pow(10, -$precision)`, наприклад, для точності `precision`, що дорівнює -1, число `num` округляється до десятків, для точності `precision`, Рівною -2, - До сотень і т. д.

`mode`

Щоб задати режим заокруглення, вказують одну з наступних констант:

| Константы | Опис |
| --- | --- |
| **`PHP_ROUND_HALF_UP`** | Округлює позитивне число `num` в більшу сторону, а негативне в меншу, перетворюючи 1.5 на 2 і -1.5 на -2 (прагне від нуля). |
| **`PHP_ROUND_HALF_DOWN`** | Округлює позитивне число `num` у меншу сторону, а негативне на більшу, перетворюючи 1.5 на 1 і -1.5 на -1 (прагне до нуля). |
| **`PHP_ROUND_HALF_EVEN`** | Округлює число `num` до найближчого парного значення, перетворюючи 1.5 та 2.5 на 2. |
| **`PHP_ROUND_HALF_ODD`** | Округлює число `num` до найближчого непарного значення, перетворюючи 1.5 на 1 і 2.5 на 3. |

### Значення, що повертаються

Повертає у вигляді числа з плаваючою точкою (float) значення, заокруглене до заданої параметром `precision` точності.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`num` більше не приймає внутрішні об'єкти, що підтримують числове перетворення. |

### Приклади

**Приклад #1 Приклад використання функції** round()\*\*\*\*

```php
<?php

var_dump(round(3.4));
var_dump(round(3.5));
var_dump(round(3.6));
var_dump(round(3.6, 0));
var_dump(round(5.045, 2));
var_dump(round(5.055, 2));
var_dump(round(345, -2));
var_dump(round(345, -3));
var_dump(round(678, -2));
var_dump(round(678, -3));

?>
```

Результат виконання наведеного прикладу:

```
float(3)
float(4)
float(4)
float(4)
float(5.05)
float(5.06)
float(300)
float(0)
float(700)
float(1000)
```

**Приклад #2 Как параметр`precision` впливає на числа з плаваючою точкою**

```php
<?php

$number = 135.79;

var_dump(round($number, 3));
var_dump(round($number, 2));
var_dump(round($number, 1));
var_dump(round($number, 0));
var_dump(round($number, -1));
var_dump(round($number, -2));
var_dump(round($number, -3));

?>
```

Результат виконання наведеного прикладу:

```
float(135.79)
float(135.79)
float(135.8)
float(136)
float(140)
float(100)
float(0)
```

**Приклад #3 Приклад використання параметра `mode`**

```php
<?php

echo 'Режимы округления с 9.5' . PHP_EOL;
var_dump(round(9.5, 0, PHP_ROUND_HALF_UP));
var_dump(round(9.5, 0, PHP_ROUND_HALF_DOWN));
var_dump(round(9.5, 0, PHP_ROUND_HALF_EVEN));
var_dump(round(9.5, 0, PHP_ROUND_HALF_ODD));

echo PHP_EOL;
echo 'Режимы округления с 8.5' . PHP_EOL;
var_dump(round(8.5, 0, PHP_ROUND_HALF_UP));
var_dump(round(8.5, 0, PHP_ROUND_HALF_DOWN));
var_dump(round(8.5, 0, PHP_ROUND_HALF_EVEN));
var_dump(round(8.5, 0, PHP_ROUND_HALF_ODD));

?>
```

Результат виконання наведеного прикладу:

```
Режимы округления с 9.5
float(10)
float(9)
float(10)
float(9)

Режимы округления с 8.5
float(9)
float(8)
float(8)
float(9)
```

**Приклад #4 Приклад використання параметра `mode` із зазначенням точності `precision`**

```php
<?php

echo 'Округление с точностью до 1 знака с константой PHP_ROUND_HALF_UP в качестве значения режима округления' . PHP_EOL;
var_dump(round( 1.55, 1, PHP_ROUND_HALF_UP));
var_dump(round(-1.55, 1, PHP_ROUND_HALF_UP));

echo PHP_EOL;
echo 'Округление с точностью до 1 знака с константой PHP_ROUND_HALF_DOWN в качестве значения режима округления' . PHP_EOL;
var_dump(round( 1.55, 1, PHP_ROUND_HALF_DOWN));
var_dump(round(-1.55, 1, PHP_ROUND_HALF_DOWN));

echo PHP_EOL;
echo 'Округление с точностью до 1 знака с константой PHP_ROUND_HALF_EVEN в качестве значения режима округления' . PHP_EOL;
var_dump(round( 1.55, 1, PHP_ROUND_HALF_EVEN));
var_dump(round(-1.55, 1, PHP_ROUND_HALF_EVEN));

echo PHP_EOL;
echo 'Округление с точностью до 1 знака с константой PHP_ROUND_HALF_ODD в качестве значения режима округления' . PHP_EOL;
var_dump(round( 1.55, 1, PHP_ROUND_HALF_ODD));
var_dump(round(-1.55, 1, PHP_ROUND_HALF_ODD));

?>
```

Результат виконання наведеного прикладу:

```
Округление с точностью до 1 знака с константой PHP_ROUND_HALF_UP в качестве значения режима округления
float(1.6)
float(-1.6)

Округление с точностью до 1 знака с константой PHP_ROUND_HALF_DOWN в качестве значения режима округления
float(1.5)
float(-1.5)

Округление с точностью до 1 знака с константой PHP_ROUND_HALF_EVEN в качестве значения режима округления
float(1.6)
float(-1.6)

Округление с точностью до 1 знака с константой PHP_ROUND_HALF_ODD в качестве значения режима округления
float(1.5)
float(-1.5)
```

### Дивіться також

-   [ceil()](function.ceil.md) \- Округлює дробове число в більшу сторону
-   [floor()](function.floor.md) \- Округлює дробове число у менший бік
-   [number\_format()](function.number-format.md) \- Форматує число з поділом груп
