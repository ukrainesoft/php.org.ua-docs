---
navigation:
  - function.strtr.md: « strtr
  - function.substr-count.md: substr\_count »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: substr\_compare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# substr\_compare

(PHP 5, PHP 7, PHP 8)

substr\_compare - Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру

### Опис

```methodsynopsis
substr_compare(    string $haystack,    string $needle,    int $offset,    ?int $length = null,    bool $case_insensitive = false): int
```

\*\*substr\_compare()\*\*сравнивает строку`haystack` (починаючи з позиції `offset`) з рядком `needle`В сравнении участвуют максимум`length` символів.

### Список параметрів

`haystack`

Основний порівнюваний рядок.

`needle`

Наступний порівнюваний рядок.

`offset`

Стартова позиція порівняння. Якщо негативна, позначає зміщення з кінця рядка.

`length`

Довжина порівняння. За замовчуванням використовується максимальна з довжин `needle`и`haystack`минус`offset`

`case_insensitive`

Якщо `case_insensitive`имеет значение\*\*`true`\*\*, Порівняння виконується без урахування регістру.

### Значення, що повертаються

Повертає `-1`, якщо `string1`меньше`string2` , якщо `string1`больше`string2`, и якщо рядки рівні. Якщо `offset` більше (до PHP 7.2.18, 7.3.5) або дорівнює довжині `haystack`или`length` переданий і менше 0, **substr\_compare()** виводить попередження та повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функція тепер повертає `-1`или ; раніше вона повертала негативне чи позитивне число. |
| 8.0.0 | `length` тепер допускає значення null. |
| 7.2.18, 7.3.5 | `offset` тепер може бути рівним `haystack` |

### Приклади

**Пример #1 Пример использования**substr\_compare()\*\*\*\*

```php
<?php
echo substr_compare("abcde", "bc", 1, 2); // 0
echo substr_compare("abcde", "de", -2, 2); // 0
echo substr_compare("abcde", "bcg", 1, 2); // 0
echo substr_compare("abcde", "BC", 1, 2, true); // 0
echo substr_compare("abcde", "bc", 1, 3); // 1
echo substr_compare("abcde", "cd", 1, 2); // -1
echo substr_compare("abcde", "abc", 5, 1); // предупреждение
?>
```

### Дивіться також

-   [strncmp()](function.strncmp.md) \- Бінарно-безпечне порівняння перших n символів рядків
