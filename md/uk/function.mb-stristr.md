---
navigation:
  - function.mb-stripos.md: « mb\_stripos
  - function.mb-strlen.md: mb\_strlen »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_stristr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_stristr

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

mb\_stristr — Знаходить перше входження підрядки в рядок без урахування регістру

### Опис

```methodsynopsis
mb_stristr(    string $haystack,    string $needle,    bool $before_needle = false,    ?string $encoding = null): string|false
```

Функция**mb\_stristr()**находит первое вхождение подстроки`needle` у рядок `haystack` і повертає частину `haystack`Функция**mb\_stristr()**, в отличие от функции[mb\_strstr()](function.mb-strstr.md), не враховує регістр. Якщо підрядок `needle` не знайдено, повертається **`false`**

### Список параметрів

`haystack`

Рядок, з якого можна отримати перше входження підрядка `needle`

`needle`

Подстрока для поиска в строке`haystack`

`before_needle`

Визначає, яку частину рядка `haystack` поверне ця функція. Якщо встановлено **`true`**, повертається частина рядка `haystack`от начала до первого вхождения подстроки`needle`(исключая подстроку). Если установлено\*\*`false`\*\*, повертається частина рядка `haystack` від першого входження підрядка `needle` до кінця (включаючи підрядок).

`encoding`

Назва кодування символів. Якщо цей параметр опущено, буде використано внутрішнє кодування символів.

### Значення, що повертаються

Повертає частину рядка `haystack`или\*\*`false`\*\*, якщо підрядок `needle`не найдена.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `needle` тепер приймає порожній рядок. |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [stristr()](function.stristr.md) \- Реєстронезалежний варіант функції strstr
-   [strstr()](function.strstr.md) \- Знаходить перше входження підрядка
-   [mb\_strstr()](function.mb-strstr.md) \- Знаходить перше входження підрядка у рядку
