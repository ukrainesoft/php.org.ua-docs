---
navigation:
  - class.random-engine-xoshiro256starstar.md: « Random\\Engine\\Xoshiro256StarStar
  - random-engine-xoshiro256starstar.debuginfo.md: 'Random\\Engine\\Xoshiro256StarStar::\_\_debugInfo »'
  - index.md: PHP Manual
  - class.random-engine-xoshiro256starstar.md: Random\\Engine\\Xoshiro256StarStar
title: 'Random\\Engine\\Xoshiro256StarStar::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Engine\\Xoshiro256StarStar::\_\_construct

(PHP 8 >= 8.2.0)

Random\\Engine\\Xoshiro256StarStar::\_\_construct - Створює новий об'єкт двигуна xoshiro256\*\*

### Опис

public **Random\\Engine\\Xoshiro256StarStar::\_\_construct**(string|int|null`$seed` **`null`**) .

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`seed`

Спосіб заповнення внутрішнього 256-бітного (32 байти) стану, що складається з чотирьох 64-бітних цілих чисел без знака, залежить від типу, що використовується як параметр `seed`

| Type | Опис |
| --- | --- |
| null | Заповнює стан 32 випадковими байтами, що згенеровані за допомогою CSPRNG. |
| int | Заповнює стан чотирма послідовними значеннями, що згенеровані за допомогою алгоритму SplitMix64, який був заповнений параметром `seed`, що інтерпретується як 64-бітове ціле число без знака. |
| string | Заповнює стан, інтерпретуючи 32-байтовий рядок (string) як чотири 64-бітові цілих числа без знака. |

### Помилки

-   Якщо довжина рядка (string) параметра`seed`не дорівнює 32 байтам, буде викинута помилка[ValueError](class.valueerror.md)
-   Якщо рядок (string) параметра`seed`складається з 32 нульових байтів (`"\x00"`), буде викинута помилка[ValueError](class.valueerror.md)

### Приклади

**Приклад #1 Приклад використання** Random\\Engine\\Xoshiro256StarStar::\_\_construct()\*\*\*\*

```php
<?php
// Использование случайного 256-битного значения.
$e = new \Random\Engine\Xoshiro256StarStar();

$r = new \Random\Randomizer($e);
?>
```

**Приклад #2 Виведення значення рядка (string)**

```php
<?php
$string = "My string seed";

// Хеширование строки с помощью SHA-256, используя двоичный вывод, чтобы превратить
// $string в 256-битное значение. Использование одной и той же строки приведёт
// к одной и той же последовательности случайностей.
$e = new \Random\Engine\Xoshiro256StarStar(
    hash('sha256', $string, binary: true)
);

echo bin2hex($e->generate()), "\n";
?>
```

Результат виконання наведеного прикладу:

```
6e013453678388c2
```
