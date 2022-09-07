---
navigation:
  - function.str-ireplace.md: « strireplace
  - function.str-repeat.md: strrepeat »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strpad
---
# strpad

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

strpad — Доповнює рядок іншим рядком до заданої довжини

### Опис

```methodsynopsis
str_pad(    string $string,    int $length,    string $pad_string = " ",    int $pad_type = STR_PAD_RIGHT): string
```

Ця функція повертає рядок `string`, доповнену ліворуч, праворуч або з обох боків до заданої довжини. Якщо необов'язковий аргумент `pad_string` не передано, то `string` буде доповнено пробілами, інакше він буде доповнений символами з `pad_string` до потрібної довжини.

### Список параметрів

`string`

Вхідний рядок.

`length`

Якщо значення `length` негативно, менше або дорівнює довжині вхідного рядка, то доповнення не відбувається і повертається вихідний рядок `string`

`pad_string`

> **Зауваження**
> 
> `pad_string` може бути урізана, якщо необхідна кількість символів, що доповнюються, не ділиться націло на довжину рядка `pad_string`

`pad_type`

Необов'язковий аргумент `pad_type` може мати значення **`STR_PAD_RIGHT`** **`STR_PAD_LEFT`** або **`STR_PAD_BOTH`**. Якщо не вказано, то за замовчуванням використовується **`STR_PAD_RIGHT`**

### Значення, що повертаються

Повертає доповнений рядок.

### Приклади

**Приклад #1 Приклад використання **strpad()****

```php
<?php
$input = "Alien";
echo str_pad($input, 10);                      // выводит "Alien     "
echo str_pad($input, 10, "-=", STR_PAD_LEFT);  // выводит "-=-=-Alien"
echo str_pad($input, 10, "_", STR_PAD_BOTH);   // выводит "__Alien___"
echo str_pad($input,  6, "___");               // выводит "Alien_"
echo str_pad($input,  3, "*");                 // выводит "Alien"
?>
```
