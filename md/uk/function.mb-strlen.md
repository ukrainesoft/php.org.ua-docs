---
navigation:
  - function.mb-stristr.md: « mb\_stristr
  - function.mb-strpos.md: mb\_strpos »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_strlen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_strlen

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_strlen — Отримує довжину рядка

### Опис

```methodsynopsis
mb_strlen(string $string, ?string $encoding = null): int
```

Отримує довжину рядка (string).

### Список параметрів

`string`

Рядок (string), на яку вимірюється довжина.

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

### Значення, що повертаються

Повертає кількість символів у рядку (string) `string`, що мають кодування символів `encoding`. Багатобайтовий символ обчислюється як один.

### Помилки

Якщо кодування невідоме, видається помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [mb\_internal\_encoding()](function.mb-internal-encoding.md) \- Встановлює/отримує внутрішнє кодування скрипту
-   [grapheme\_strlen()](function.grapheme-strlen.md) \- отримує довжину рядка в одиницях графеми
-   [iconv\_strlen()](function.iconv-strlen.md) \- Повертає кількість символів у рядку
-   [strlen()](function.strlen.md) \- Повертає довжину рядка
