---
navigation:
  - function.mb-strlen.md: « mb\_strlen
  - function.mb-strrchr.md: mb\_strrchr »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_strpos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_strpos

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_strpos — Шукає позицію першого входження підрядка в рядок

### Опис

```methodsynopsis
mb_strpos(    string $haystack,    string $needle,    int $offset = 0,    ?string $encoding = null): int|false
```

Знаходить позицію першого входження підрядка (string) у рядок (string).

Виконує безпечну багатобайтову операцію [strpos()](function.strpos.md), яка спирається на число символів у рядку. Перший символ стоїть позиції 0, позиція другого 1 тощо.

### Список параметрів

`haystack`

Рядок (string), в якому функція шукатиме підрядок.

`needle`

Підрядок, який потрібно знайти у рядку `haystack`. Порівняно з функцією [strpos()](function.strpos.md), ця функція не використовує числові значення як порядкові значення символів.

`offset`

Зміщення початку пошуку. Якщо не заданий, приймає значення 0. Негативне усунення відраховується від кінця рядка.

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

### Значення, що повертаються

Повертає число - позицію першого входження підрядка `needle`в строку (string)`haystack`. Якщо підрядок `needle` не знайдено, повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `needle` тепер приймає порожній рядок. |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |
| 7.1.0 | В параметре`offset` додано підтримку негативних значень. |

### Дивіться також

-   [mb\_internal\_encoding()](function.mb-internal-encoding.md) \- Встановлює/отримує внутрішнє кодування скрипту
-   [strpos()](function.strpos.md) \- Повертає позицію першого входження підрядка
