Розархівація LZF

-   [« lzfcompress](function.lzf-compress.html)
    
-   [lzfoptimizedfor »](function.lzf-optimized-for.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LZF](ref.lzf.html)
    
-   Розархівація LZF
    

# lzfdecompress

(PECL lzf >= 0.1.0)

lzfdecompress — Розархівація LZF

### Опис

```methodsynopsis
lzf_decompress(string $data): string
```

[lzfcompress()](function.lzf-compress.html) розархівує рядок `data`, Що містить дані стиснуті алгоритмом lzf

### Список параметрів

`data`

Рядок зі стислими даними.

### Значення, що повертаються

Повертає розархівовані дані або **`false`** у разі виникнення помилки.

### Дивіться також

-   [lzfcompress()](function.lzf-compress.html) - Стиснення LZF