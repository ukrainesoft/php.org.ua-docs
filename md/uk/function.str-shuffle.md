---
navigation:
  - function.str-rot13.html: « strrot13
  - function.str-split.html: strsplit »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: strshuffle
---
# strshuffle

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

strshuffle — Переставляє символи у рядку випадковим чином

### Опис

```methodsynopsis
str_shuffle(string $string): string
```

**strshuffle()** перемішує символи у рядку. Вибирається одна можлива перестановка із усіх можливих.

**Застереження**

Ця функція не генерує криптографічно безпечні значення і не повинна використовуватись у криптографічних цілях. Якщо вам потрібне криптографічно безпечне значення, подумайте про використання функцій [randomint()](function.random-int.html) [randombytes()](function.random-bytes.html) або [opensslrandompseudobytes()](function.openssl-random-pseudo-bytes.html) замість цієї.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає перемішаний рядок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Внутрішній алгоритм отримання випадкових чисел [изменён](migration71.incompatible.html#migration71.incompatible.rand-srand-aliases) з функції rand бібліотеки libc на генератор на базі [» Вихря Мерсена](http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.html) |

### Приклади

**Приклад #1 Приклад використання **strshuffle()****

```php
<?php
$str = 'abcdef';
$shuffled = str_shuffle($str);

// выведет что-то вроде этого: bfdaec
echo $shuffled;
?>
```

### Дивіться також

-   [shuffle()](function.shuffle.html) - перемішує масив
-   [rand()](function.rand.html) - Генерує випадкове число
