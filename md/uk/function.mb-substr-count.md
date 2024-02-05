---
navigation:
  - function.mb-substitute-character.md: « mb\_substitute\_character
  - function.mb-substr.md: mb\_substr »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_substr\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_substr\_count

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

mb\_substr\_count — Повертає кількість входжень підрядка

### Опис

```methodsynopsis
mb_substr_count(string $haystack, string $needle, ?string $encoding = null): int
```

Підраховує, скільки разів підрядок `needle` зустрічається у рядку `haystack`

### Список параметрів

`haystack`

Рядок (string) для перевірки.

`needle`

Рядок (string) для пошуку.

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

### Значення, що повертаються

Повертає кількість входжень підрядка `needle` у рядок `haystack`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад использования функции**mb\_substr\_count()\*\*\*\*

```php
<?php
echo mb_substr_count("Это просто проверка", "то"); // выведет на экран 2
?>
```

### Дивіться також

-   [mb\_strpos()](function.mb-strpos.md) \- Шукає позицію першого входження підрядка у рядок
-   [mb\_substr()](function.mb-substr.md) \- Повертає частину рядка
-   [substr\_count()](function.substr-count.md) \- Повертає кількість входжень підрядка
