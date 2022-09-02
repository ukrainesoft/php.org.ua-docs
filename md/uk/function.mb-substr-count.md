---
navigation:
  - function.mb-substitute-character.md: « mbsubstitutecharacter
  - function.mb-substr.md: мбsubstr »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбsubstrcount
---
# мбsubstrcount

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

мбsubstrcount — Повертає кількість входжень підрядка

### Опис

```methodsynopsis
mb_substr_count(string $haystack, string $needle, ?string $encoding = null): int
```

Підраховує, скільки разів підрядок `needle` зустрічається у рядку `haystack`

### Список параметрів

`haystack`

Рядок (string) для перевірки

`needle`

Рядок (string) для пошуку

`encoding`

Параметр `encoding` є символьним кодуванням. Якщо він опущений або дорівнює **`null`**, замість нього буде використано значення внутрішнього кодування.

### Значення, що повертаються

Кількість входжень підрядка `needle` у рядок `haystack`

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання **мбsubstrcount()****

```php
<?php
echo mb_substr_count("Это просто проверка", "то"); // выведет на экран 2
?>
```

### Дивіться також

-   [мбstrpos()](function.mb-strpos.md) - Пошук позиції першого входження одного рядка до іншого
-   [мбsubstr()](function.mb-substr.md) - Повертає частину рядка
-   [substrcount()](function.substr-count.md) - Повертає кількість входжень підрядка
