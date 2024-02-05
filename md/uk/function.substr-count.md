---
navigation:
  - function.substr-compare.md: « substr\_compare
  - function.substr-replace.md: substr\_replace »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: substr\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# substr\_count

(PHP 4, PHP 5, PHP 7, PHP 8)

substr\_count — Повертає кількість входжень підрядка

### Опис

```methodsynopsis
substr_count(    string $haystack,    string $needle,    int $offset = 0,    ?int $length = null): int
```

**substr\_count()** повертає кількість входжень підрядка `needle` у рядок `haystack`Заметьте, что параметр`needle`чувствителен к регистру.

> **Зауваження** :
> 
> Ця функція не підраховує підстроки, що перекриваються. Дивіться приклад нижче!

### Список параметрів

`haystack`

Рядок, в якому ведеться пошук

`needle`

Шуканий підрядок

`offset`

Усунення початку відліку. Якщо задано негативне значення, відлік позиції буде здійснено з кінця рядка.

`length`

Максимальна довжина рядка, в якій буде здійснюватися пошук підрядка після вказаного усунення. Якщо сума зміщення та максимальної довжини буде більшою за довжину `haystack`, то буде виведено попередження. Негативне значення буде відраховуватись з кінця `haystack`

### Значення, що повертаються

Ця функція повертає цілу кількість (int).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `length` тепер допускає значення null. |
| 7.1.0 | Додано підтримку негативних значень `offset`и`length`. . `length` тепер також може бути |

### Приклади

**Пример #1 Пример использования**substr\_count()\*\*\*\*

```php
<?php
$text = 'This is a test';
echo strlen($text); // 14

echo substr_count($text, 'is'); // 2

// строка уменьшается до 's is a test', поэтому вывод будет 1
echo substr_count($text, 'is', 3);

// текст уменьшается до 's i', поэтому вывод будет 0
echo substr_count($text, 'is', 3, 3);

// генерирует предупреждение, так как  5+10 > 14
echo substr_count($text, 'is', 5, 10);


// выводит только 1, т.к. перекрывающиеся подстроки не учитываются
$text2 = 'gcdgcdgcd';
echo substr_count($text2, 'gcdgcd');
?>
```

### Дивіться також

-   [count\_chars()](function.count-chars.md) \- Повертає інформацію про символи, що входять до рядка
-   [strpos()](function.strpos.md) \- Повертає позицію першого входження підрядка
-   [substr()](function.substr.md) \- Повертає підрядок
-   [strstr()](function.strstr.md) \- Знаходить перше входження підрядка
