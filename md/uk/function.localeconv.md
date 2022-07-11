- [Levenshtein](function.levenshtein.md)
- [ltrim »](function.ltrim.md)

- [PHP Manual](index.md)
- [Функції для роботи з рядками](ref.strings.md)
- Повертає інформацію про форматування чисел

#localeconv

(PHP 4 \>= 4.0.5, PHP 5, PHP 7, PHP 8)

localeconv — Повертає інформацію про форматування чисел

### Опис

**localeconv**(): array

Повертає асоціативний масив з інформацією про числові та грошові
форматах у поточній локалі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**localeconv()** повертає дані, засновані на поточній локалі,
встановленою функцією [setlocale()](function.setlocale.md).
Повертається масив містить такі елементи:

[TABLE]

`p_sign_posn` та `n_sign_posn` містять рядок з опціями форматування.
Кожне число є однією з перерахованих вище умов.

Елементи угруповання містять масиви, які описують спосіб
угруповання цифр. Наприклад, поле угруповання грошових величин у локалі
nl_NL (у режимі UTF-8 зі знаком євро) містить масив із двох елементів
зі значеннями 3 та 3. Більший індекс масиву відповідає угрупованню
цифр, розташованих ліворуч. Якщо елемент масиву дорівнює **`CHAR_MAX`**,
наступні цифри не групуються. Якщо елемент масиву дорівнює 0,
використовується значення попереднього елемента.

### Приклади

**Приклад #1 Приклад використання **localeconv()****

` <?phpif (false !== setlocale(LC_ALL, 'ru_RU.UTF-8')) {   $locale_info = localeconv(); print_r($locale_info);}?> `

Результат виконання цього прикладу:

Array
(
[decimal_point] => ,
[thousands_sep] =>
[int_curr_symbol] => RUB
[currency_symbol] => руб
[mon_decimal_point] =>.
[mon_thousands_sep] =>
[positive_sign] =>
[negative_sign] => -
[int_frac_digits] => 2
[frac_digits] => 2
[p_cs_precedes] => 0
[p_sep_by_space] => 1
[n_cs_precedes] => 0
[n_sep_by_space] => 1
[p_sign_posn] => 1
[n_sign_posn] => 1
[grouping] => Array
(
[0] => 3
[1] => 3
)

[mon_grouping] => Array
(
[0] => 3
[1] => 3
)

)

### Дивіться також

- [setlocale()](function.setlocale.md) - Встановлює налаштування
локалі
