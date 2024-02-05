---
navigation:
  - function.mb-strripos.md: « mb\_strripos
  - function.mb-strstr.md: mb\_strstr »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_strrpos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_strrpos

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_strrpos — Шукає позицію останнього входження підрядка в рядок

### Опис

```methodsynopsis
mb_strrpos(    string $haystack,    string $needle,    int $offset = 0,    ?string $encoding = null): int|false
```

Виконує безпечну багатобайтову операцію [strrpos()](function.strrpos.md), ґрунтуючись на кількості символів. Позиція підрядка `needle` розраховується з початку рядка `haystack`Позиция первого символа — 0. Второго символа — 1.

### Список параметрів

`haystack`

Рядок (string), в якому функція шукатиме останнє входження підрядка `needle`

`needle`

Подстрока (string) для поиска в строке`haystack`

`offset`

Може бути вказано для початку пошуку довільної кількості символів у рядку (string). Негативні значення припинять пошук довільної точки до кінця рядка (string).

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

### Значення, що повертаються

Повертає позицію останнього входження підрядка `needle`в строку (string)`haystack`либо\*\*`false`\*\*, якщо підрядок `needle`не найдена.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `needle` тепер приймає порожній рядок. |
| 8.0.0 | Передача кодування символів `encoding` як третій аргумент замість offset було видалено. |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [mb\_strpos()](function.mb-strpos.md) \- Шукає позицію першого входження підрядка у рядок
-   [mb\_internal\_encoding()](function.mb-internal-encoding.md) \- Встановлює/отримує внутрішнє кодування скрипту
-   [strrpos()](function.strrpos.md) \- Повертає позицію останнього входження підрядка у рядку
