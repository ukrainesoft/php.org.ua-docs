Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру

-   [« strtr](function.strtr.html)
    
-   [substrcount »](function.substr-count.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з рядками](ref.strings.html)
    
-   Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
    

# substrcompare

(PHP 5, PHP 7, PHP 8)

substrcompare — Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру

### Опис

```methodsynopsis
substr_compare(    string $haystack,    string $needle,    int $offset,    ?int $length = null,    bool $case_insensitive = false): int
```

**substrcompare()** порівнює рядок `haystack` (починаючи з позиції `offset`) з рядком `needle`. У порівнянні беруть участь максимум `length` символів.

### Список параметрів

`haystack`

Основний порівнюваний рядок.

`needle`

Наступний порівнюваний рядок.

`offset`

Стартова позиція порівняння. Якщо негативна, позначає зміщення з кінця рядка.

`length`

Довжина порівняння. За замовчуванням використовується максимальна з довжин `needle` і `haystack` мінус `offset`

`case_insensitivity`

Якщо `case_insensitivity` має значення **`true`**, Порівняння виконується без урахування регістру.

### Значення, що повертаються

Повертає від'ємне число, якщо рядок `haystack` (починаючи з символу `offset`) менше ніж `needle`; позитивне число, якщо вона більша `needle`; 0, якщо рядки дорівнюють. Якщо `offset` більше (до PHP 7.2.18, 7.3.5) або дорівнює довжині `haystack` або `length` переданий і менше 0, **substrcompare()** виводить попередження та повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `length` тепер допускає значення null. |
|  | `offset` тепер може бути рівним `haystack` |

### Приклади

**Приклад #1 Приклад використання **substrcompare()****

```php
<?php
echo substr_compare("abcde", "bc", 1, 2); // 0
echo substr_compare("abcde", "de", -2, 2); // 0
echo substr_compare("abcde", "bcg", 1, 2); // 0
echo substr_compare("abcde", "BC", 1, 2, true); // 0
echo substr_compare("abcde", "bc", 1, 3); // 1
echo substr_compare("abcde", "cd", 1, 2); // -1
echo substr_compare("abcde", "abc", 5, 1); // предупреждение
?>
```

### Дивіться також

-   [strncmp()](function.strncmp.html) - Бінарно-безпечне порівняння перших n символів рядків