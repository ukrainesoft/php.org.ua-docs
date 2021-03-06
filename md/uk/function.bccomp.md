- [«bcadd](function.bcadd.md)
- [bcdiv »](function.bcdiv.md)

- [PHP Manual](index.md)
- [Функції BC Math](ref.bc.md)
- Порівняння двох чисел довільної точності

#bccomp

(PHP 4, PHP 5, PHP 7, PHP 8)

bccomp — Порівняння двох чисел довільної точності

### Опис

**bccomp**(string `$num1`, string `$num2`, ?int `$scale` = **`null`**):
int

Порівнює `num1` з `num2` і повертає цілий результат.

### Список параметрів

`num1`
Лівий операнд у вигляді рядка.

`num2`
Правий операнд у вигляді рядка.

`scale`
Необов'язковий аргумент `scale` задає кількість цифр після десяткової
точки, яка братиме участь у порівнянні.

### Значення, що повертаються

Повертає 0 якщо числа рівні; 1, якщо `left_operand` більше, ніж
`right_operand`; -1, якщо менше.

### Список змін

| Версія | Опис                                 |
| ------ | ------------------------------------ |
| 8.0.0  | scale тепер припускає значення null. |

### Приклади

**Приклад #1 Приклад використання **bccomp()****

`<?phpecho bccomp('1', '2') . "
";   // -1echo bccomp('1.00001', '1', 3); // 0echo bccomp('1.00001', '1', 5); // 1?> `
