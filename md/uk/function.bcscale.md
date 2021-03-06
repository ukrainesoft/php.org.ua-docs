- [«bcpowmod](function.bcpowmod.md)
- [bcsqrt »](function.bcsqrt.md)

- [PHP Manual](index.md)
- [Функції BC Math](ref.bc.md)
- Встановлює чи отримує кількість чисел після десяткової точки
за замовчуванням для всіх функцій bc math.

#bcscale

(PHP 4, PHP 5, PHP 7, PHP 8)

bcscale — Встановлює чи отримує кількість чисел після десяткової
стандартні точки для всіх функцій bc math.

### Опис

**bcscale**(int `$scale`): int

Задає кількість чисел після десяткової точки за промовчанням для функцій
bc math, які не можуть явно отримати це число як аргумент.

**bcscale**(null `$scale` = **`null`**): int

Отримує поточний масштаб.

### Список параметрів

`scale`
Масштаб, кількість знаків після коми.

### Значення, що повертаються

Повертає старий масштаб, якщо використовується як сетер. В протилежному
У разі повертає поточний масштаб.

### Список змін

| Версія | Опис                                                                                                                                                                                                                   |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8.0.0  | scale is now nullable.                                                                                                                                                                                                 |
| 7.3.0  | **bcscale()** тепер можна використовувати для отримання поточного масштабу; при встановленні нового значення поверне старе значення масштабу. Раніше scale був обов'язковим, і **bcscale()** завжди повертав **true**. |

### Приклади

**Приклад #1 Приклад використання **bcscale()****

`<?php// масштаб за мовчанням : 3bcscale(3);echo bcdiv('105', '6.55957'); // 16.007// то же саме без bcscale()echo bcdiv('105', '6.55957', 3); // 16.007?> `
