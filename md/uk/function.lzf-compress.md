---
navigation:
  - ref.lzf.md: « Функції LZF
  - function.lzf-decompress.html: lzfdecompress »
  - index.md: PHP Manual
  - ref.lzf.md: Функції LZF
title: lzfcompress
---
# lzfcompress

(PECL lzf >= 0.1.0)

lzfcompress — Стиснення LZF

### Опис

```methodsynopsis
lzf_compress(string $data): string
```

**lzfcompress()** стискає рядок даних `data` Використовуючи алгоритм LZF.

### Список параметрів

`data`

Рядок для стиснення.

### Значення, що повертаються

Повертає стислі дані або **`false`** у разі виникнення помилки.

### Дивіться також

-   [lzfdecompress()](function.lzf-decompress.html) - Розархівація LZF
