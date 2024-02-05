---
navigation:
  - function.gzcompress.md: « gzcompress
  - function.gzdeflate.md: gzdeflate »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzdecode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzdecode

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

gzdecode — Декодує рядок, стиснутий за допомогою gzip

### Опис

```methodsynopsis
gzdecode(string $data, int $max_length = 0): string|false
```

Ця функція повертає декодовану версію вхідних даних . `data`

### Список параметрів

`data`

Дані для декодування, закодовані за допомогою [gzencode()](function.gzencode.md)

`max_length`

Максимальний розмір рядка для декодування.

### Значення, що повертаються

Розпакований рядок або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

У разі виникнення помилки повертає помилку рівня **`E_WARNING`**

### Дивіться також

-   [gzencode()](function.gzencode.md) \- Створити стислий рядок gzip
