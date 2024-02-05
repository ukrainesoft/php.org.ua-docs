---
navigation:
  - function.mb-strrichr.md: « mb\_strrichr
  - function.mb-strrpos.md: mb\_strrpos »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_strripos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_strripos

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

mb\_strripos — Знаходить останнє входження підрядка в рядок без урахування регістру

### Опис

```methodsynopsis
mb_strripos(    string $haystack,    string $needle,    int $offset = 0,    ?string $encoding = null): int|false
```

Функция**mb\_strripos()** виконує безпечну багатобайтову операцію [strripos()](function.strripos.md), ґрунтуючись на кількості символів. Позиція підрядка `needle` розраховується з початку рядка `haystack`Позиция первого символа — 0. Второго символа — 1. Функция**mb\_strripos()**, в отличие от функции[mb\_strrpos()](function.mb-strrpos.md)не чутлива до регістру.

### Список параметрів

`haystack`

Рядок, в якому функція шукатиме позицію останнього входження підрядка `needle`

`needle`

Подстрока для поиска в строке`haystack`

`offset`

Позиция в строке`haystack`, з якої потрібно розпочати пошук.

`encoding`

Назва кодування символів. Якщо на задане, буде використано внутрішнє кодування символів.

### Значення, що повертаються

Повертає число — позицію останнього входження підрядка `needle` у рядок `haystack`либо\*\*`false`\*\*, якщо підрядок `needle`не найдена.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `needle` тепер приймає порожній рядок. |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [strripos()](function.strripos.md) \- Повертає позицію останнього входження підрядка без урахування регістру
-   [strrpos()](function.strrpos.md) \- Повертає позицію останнього входження підрядка у рядку
-   [mb\_strrpos()](function.mb-strrpos.md) \- Шукає позицію останнього входження підрядка у рядок
