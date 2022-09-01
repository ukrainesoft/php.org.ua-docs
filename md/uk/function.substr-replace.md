---
navigation:
  - function.substr-count.html: « substrcount
  - function.substr.html: substr »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: substrreplace
---
# substrreplace

(PHP 4, PHP 5, PHP 7, PHP 8)

substrreplace — Замінює частину рядка

### Опис

```methodsynopsis
substr_replace(    array|string $string,    array|string $replace,    array|int $offset,    array|int|null $length = null): string|array
```

**substrreplace()** замінює частину рядка `string`, що починається із символу з порядковим номером `offset` та (необов'язковою) довжиною `length`, рядком `replace` та повертає результат.

### Список параметрів

`string`

Вхідний рядок.

Також можна вказати масив рядків, у цьому випадку заміни відбуватимуться з кожним наданим рядком. У цьому випадку параметри `replace` `offset` і `length` можуть бути як скалярними значеннями – у цьому випадку ці значення будуть застосовані до кожного рядка, так і масивами – у цьому випадку відповідні елементи масивів будуть застосовані до кожного наданого рядка.

`replace`

Рядок заміни.

`offset`

Якщо `offset` позитивний, заміна починається з символу з порядковим номером `offset` рядки `string`

Якщо `offset` від'ємний, заміна починається із символу з порядковим номером `offset`, рахуючи від кінця рядка `string`

`length`

Якщо аргумент позитивний, то він являє собою довжину підрядки, що замінюється в рядку `string`. Якщо цей аргумент є негативним, він визначає кількість символів від кінця рядка `string`на яких закінчується заміна. Цей аргумент необов'язковий і за промовчанням дорівнює strlen(`string`);, тобто заміна до кінця рядка `string`. Зрозуміло, якщо `length` дорівнює нулю, то це еквівалентно вставці `replace` в `string` на вказаній позиції `offset`

### Значення, що повертаються

Повертає результуючий рядок. Якщо `string` є масивом, що повертає масив.

### список змін

| Версия | Описание |
| --- | --- |
|  | `length` тепер допускає значення null. |

### Приклади

**Приклад #1 Простий приклад використання **substrreplace()****

```php
<?php
$var = 'ABCDEFGH:/MNRPQR/';
echo "Оригинал: $var<hr />\n";

/* Обе следующих строки заменяют всю строку $var на 'bob'. */
echo substr_replace($var, 'bob', 0) . "<br />\n";
echo substr_replace($var, 'bob', 0, strlen($var)) . "<br />\n";

/* Вставляет 'bob' в начало $var. */
echo substr_replace($var, 'bob', 0, 0) . "<br />\n";

/* Обе следующих строки заменяют 'MNRPQR' в $var на 'bob'. */
echo substr_replace($var, 'bob', 10, -1) . "<br />\n";
echo substr_replace($var, 'bob', -7, -1) . "<br />\n";

/* Удаляет 'MNRPQR' из $var. */
echo substr_replace($var, '', 10, -1) . "<br />\n";
?>
```

**Приклад #2 Використання **substrreplace()** для одночасної множинної заміни рядків**

```php
<?php
$input = array('A: XXX', 'B: XXX', 'C: XXX');

// Простой случай: заменяем XXX на YYY в каждой строке.
echo implode('; ', substr_replace($input, 'YYY', 3, 3))."\n";

// Более сложный случай с уникальными заменами.
$replace = array('AAA', 'BBB', 'CCC');
echo implode('; ', substr_replace($input, $replace, 3, 3))."\n";

// Замены с разными количествами символов.
$length = array(1, 2, 3);
echo implode('; ', substr_replace($input, $replace, 3, $length))."\n";
?>
```

Результат виконання цього прикладу:

```
A: YYY; B: YYY; C: YYY
A: AAA; B: BBB; C: CCC
A: AAAXX; B: BBBX; C: CCC
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [strreplace()](function.str-replace.html) - Замінює всі входження рядка пошуку на рядок заміни
-   [substr()](function.substr.html) - Повертає підрядок
-   [Доступ к символу в строке и его изменение](language.types.string.html#language.types.string.substr)
