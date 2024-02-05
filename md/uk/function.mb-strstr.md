---
navigation:
  - function.mb-strrpos.md: « mb\_strrpos
  - function.mb-strtolower.md: mb\_strtolower »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_strstr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_strstr

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

mb\_strstr — Знаходить перше входження підрядка у рядку

### Опис

```methodsynopsis
mb_strstr(    string $haystack,    string $needle,    bool $before_needle = false,    ?string $encoding = null): string|false
```

Функция\*\*mb\_strstr()\*\*находит первое вхождение подстроки`needle` у рядок `haystack` та повертає частину рядка `haystack`. Якщо підрядок `needle` не знайдено, повертається **`false`**

### Список параметрів

`haystack`

Рядок, в якому функція шукатиме підрядок `needle`

`needle`

Подстрока для поиска в строке`haystack`

`before_needle`

Визначає, яку частину рядка `haystack` поверне ця функція. Якщо встановлено **`true`**, повертається частина рядка `haystack`от начала до первого вхождения подстроки`needle`(исключая подстроку). Если установлено\*\*`false`\*\*, повертається частина рядка `haystack` від першого входження підрядка `needle` до кінця (включаючи підрядок).

`encoding`

Назва кодування символів. Якщо цей параметр опущено, буде використано внутрішнє кодування символів.

### Значення, що повертаються

Повертає частину рядка рядка `haystack`или\*\*`false`\*\*, якщо підрядок `needle`не найдена.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `needle` тепер приймає порожній рядок. |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [stristr()](function.stristr.md) \- Реєстронезалежний варіант функції strstr
-   [strstr()](function.strstr.md) \- Знаходить перше входження підрядка
-   [mb\_stristr()](function.mb-stristr.md) \- Знаходить перше входження підрядки в рядок без урахування регістру
