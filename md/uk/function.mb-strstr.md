---
navigation:
  - function.mb-strrpos.md: « mbstrrpos
  - function.mb-strtolower.md: мбstrtolower »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбstrstr
---
# мбstrstr

(PHP 5> = 5.2.0, PHP 7, PHP 8)

мбstrstr — Знаходить перше входження підрядка у рядку

### Опис

```methodsynopsis
mb_strstr(    string $haystack,    string $needle,    bool $before_needle = false,    ?string $encoding = null): string|false
```

**мбstrstr()** знаходить перше входження підрядка `needle` у рядку `haystack` і повертає частину `haystack`. Якщо `needle` не знайдено, повертається **`false`**

### Список параметрів

`haystack`

Рядок, в якому шукається перше входження рядка `needle`

`needle`

Рядок для пошуку в `haystack`

`before_needle`

Визначає, яку частину рядка `haystack` поверне ця функція. Якщо встановлено **`true`**, повертається частина `haystack` від початку до першого входження `needle` (Виключаючи needle). Якщо встановлено **`false`**, повертається частина `haystack` від першого входження `needle` до кінця (включаючи needle).

`encoding`

Назва кодування символів, що використовується. Якщо цей параметр опущено, використовується внутрішнє кодування.

### Значення, що повертаються

Повертає частину рядка `haystack`, або **`false`**, якщо `needle` не знайдена.

### список змін

| Версия | Описание |
| --- | --- |
|  | `needle` тепер приймає порожній рядок. |
|  | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [stristr()](function.stristr.md) - Реєстронезалежний варіант функції strstr
-   [strstr()](function.strstr.md) - Знаходить перше входження підрядка
-   [мбstristr()](function.mb-stristr.md) - Знаходить перше входження підрядки у рядку без урахування регістру
