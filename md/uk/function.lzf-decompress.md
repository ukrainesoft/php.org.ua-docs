---
navigation:
  - function.lzf-compress.md: « lzf\_compress
  - function.lzf-optimized-for.md: lzf\_optimized\_for »
  - index.md: PHP Manual
  - ref.lzf.md: Функції LZF
title: lzf\_decompress
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# lzf\_decompress

(PECL lzf >= 0.1.0)

lzf\_decompress — Розархівація LZF

### Опис

```methodsynopsis
lzf_decompress(string $data): string
```

[lzf\_compress()](function.lzf-compress.md) розархівує рядок `data`, Що містить дані стиснуті алгоритмом lzf

### Список параметрів

`data`

Рядок зі стислими даними.

### Значення, що повертаються

Повертає розархівовані дані або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [lzf\_compress()](function.lzf-compress.md) \- Стиснення LZF
