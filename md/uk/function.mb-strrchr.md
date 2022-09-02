---
navigation:
  - function.mb-strpos.md: « mbstrpos
  - function.mb-strrichr.md: мбstrrichr »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбstrrchr
---
# мбstrrchr

(PHP 5> = 5.2.0, PHP 7, PHP 8)

мбstrrchr — Пошук останнього входження одного рядка до іншого

### Опис

```methodsynopsis
mb_strrchr(    string $haystack,    string $needle,    bool $before_needle = false,    ?string $encoding = null): string|false
```

**мбstrrchr()** шукає останнє входження рядка `needle` у рядку `haystack` та повертає частину рядка `haystack`. Якщо `needle` не знайдено, функція повертає **`false`**

### Список параметрів

`haystack`

Рядок, в якому проводиться пошук входження `needle`

`needle`

Рядок, пошук якого проводиться у рядку `haystack`

`before_needle`

Визначає, яку частину рядка `haystack` повернути як результат. Якщо передається **`true`**, функція поверне частину рядка `haystack` з початку до позиції останнього входження `needle`. Якщо передається **`false`**, буде повернуто частину `haystack` від позиції останнього входження `needle` до кінця рядка.

`encoding`

Кодування рядків. Якщо не встановлено, буде використано внутрішнє кодування скрипта.

### Значення, що повертаються

Повертає частину рядка `haystack` або **`false`**, якщо `needle` не знайдена.

### список змін

| Версия | Описание |
| --- | --- |
|  | `needle` тепер приймає порожній рядок. |
|  | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [strrchr()](function.strrchr.md) - Знаходить останнє входження символу у рядку
-   [мбstrstr()](function.mb-strstr.md) - Знаходить перше входження підрядка у рядку
-   [мбstrrichr()](function.mb-strrichr.md) - Пошук останнього входження одного рядка в інший, нечутливий до регістру
