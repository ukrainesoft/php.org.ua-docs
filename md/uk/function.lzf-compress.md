---
navigation:
  - ref.lzf.md: « Функції LZF
  - function.lzf-decompress.md: lzf\_decompress »
  - index.md: PHP Manual
  - ref.lzf.md: Функції LZF
title: lzf\_compress
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# lzf\_compress

(PECL lzf >= 0.1.0)

lzf\_compress — Стиснення LZF

### Опис

```methodsynopsis
lzf_compress(string $data): string
```

**lzf\_compress()** стискає рядок даних `data`используя алгоритм LZF.

### Список параметрів

`data`

Рядок для стиснення.

### Значення, що повертаються

Повертає стислі дані або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [lzf\_decompress()](function.lzf-decompress.md) \- Розархівація LZF
