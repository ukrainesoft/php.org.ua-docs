---
navigation:
  - function.lzf-compress.html: « lzfcompress
  - function.lzf-optimized-for.html: lzfoptimizedfor »
  - index.md: PHP Manual
  - ref.lzf.md: Функції LZF
title: lzfdecompress
---
# lzfdecompress

(PECL lzf >= 0.1.0)

lzfdecompress — Розархівація LZF

### Опис

```methodsynopsis
lzf_decompress(string $data): string
```

[lzfcompress()](function.lzf-compress.md) розархівує рядок `data`, Що містить дані стиснуті алгоритмом lzf

### Список параметрів

`data`

Рядок зі стислими даними.

### Значення, що повертаються

Повертає розархівовані дані або **`false`** у разі виникнення помилки.

### Дивіться також

-   [lzfcompress()](function.lzf-compress.md) - Стиснення LZF
