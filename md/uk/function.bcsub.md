- [«bcsqrt](function.bcsqrt.md)
- [GMP »](book.gmp.md)

- [PHP Manual](index.md)
- [Функції BC Math](ref.bc.md)
- Віднімає одне число з іншого із заданою точністю

#bcsub

(PHP 4, PHP 5, PHP 7, PHP 8)

bcsub — Віднімає одне число з іншого із заданою точністю

### Опис

**bcsub**(string `$num1`, string `$num2`, ?int `$scale` = **`null`**):
string

Віднімає число `num2` з `num1`.

### Список параметрів

`num1`
Лівий операнд (зменшуване) у вигляді рядка.

`num2`
Правий операнд (віднімається) у вигляді рядка.

`scale`
Цей необов'язковий параметр використовується для встановлення кількості
знаків після десяткового роздільника у результаті. Якщо не поставлено, то,
за замовчуванням, буде використано значення, задане глобально за допомогою
[bcscale()](function.bcscale.md), або `0`.

### Значення, що повертаються

Різниця у вигляді рядка.

### Список змін

| Версія | Опис                                 |
|--------|--------------------------------------|
| 8.0.0  | scale тепер припускає значення null. |

### Приклади

**Приклад #1 Приклад використання **bcsub()****

` <?php$a = '1.234';$b = '5';echo bcsub($a, $b); // -3echo bcsub($a, $b, 4); // -3.7660?> `

### Дивіться також

- [bcadd()](function.bcadd.md) - Скласти 2 числа довільної
точності
