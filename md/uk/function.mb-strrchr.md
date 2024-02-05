---
navigation:
  - function.mb-strpos.md: « mb\_strpos
  - function.mb-strrichr.md: mb\_strrichr »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_strrchr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_strrchr

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

mb\_strrchr — Знаходить останнє входження символу підрядка в рядок

### Опис

```methodsynopsis
mb_strrchr(    string $haystack,    string $needle,    bool $before_needle = false,    ?string $encoding = null): string|false
```

Функция\*\*mb\_strrchr()\*\*находит последнее вхождение подстроки`needle` у рядок `haystack` та повертає частину рядка `haystack`. Якщо підрядок `needle` не знайдено, функція повертає **`false`**

### Список параметрів

`haystack`

Рядок, в якому функція шукатиме останнє входження підрядка `needle`

`needle`

Подстрока для поиска в строке`haystack`

`before_needle`

Визначає, яку частину рядка `haystack` повернути як результат. Якщо передається **`true`**, функція поверне частину рядка `haystack`с начала до позиции последнего вхождения подстроки`needle`. Якщо передається **`false`**, буде повернуто частину рядка `haystack`от позиции последнего вхождения подстроки`needle`до конца строки.

`encoding`

Назва кодування символів. Якщо не вказано, буде використано внутрішнє кодування символів.

### Значення, що повертаються

Повертає частину рядка `haystack`либо\*\*`false`\*\*, якщо підрядок `needle`не найдена.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `needle` тепер приймає порожній рядок. |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [strrchr()](function.strrchr.md) \- Знаходить останнє входження символу у рядку
-   [mb\_strstr()](function.mb-strstr.md) \- Знаходить перше входження підрядка у рядку
-   [mb\_strrichr()](function.mb-strrichr.md) \- Знаходить останнє входження символу підрядка в рядок без урахування регістру
