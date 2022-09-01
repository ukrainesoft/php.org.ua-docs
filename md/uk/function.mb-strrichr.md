---
navigation:
  - function.mb-strrchr.html: « mbstrrchr
  - function.mb-strripos.html: мбstrripos »
  - index.html: PHP Manual
  - ref.mbstring.html: Функції для роботи з багатобайтовими рядками
title: мбstrrichr
---
# мбstrrichr

(PHP 5> = 5.2.0, PHP 7, PHP 8)

мбstrrichr — Пошук останнього входження одного рядка в інший, нечутливий до регістру

### Опис

```methodsynopsis
mb_strrichr(    string $haystack,    string $needle,    bool $before_needle = false,    ?string $encoding = null): string|false
```

**мбstrrichr()** шукає останнє входження рядка `needle` у рядку `haystack` та повертає частину рядка `haystack`. На відміну від [мбstrrchr()](function.mb-strrchr.html) **мбstrrichr()** не чутлива до регістру символів. Якщо `needle` не знайдено, функція повертає **`false`**

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

-   [мбstristr()](function.mb-stristr.html) - Знаходить перше входження підрядки у рядку без урахування регістру
-   [мбstrrchr()](function.mb-strrchr.html) - Пошук останнього входження одного рядка в інший
