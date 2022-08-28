Розархівація LZF

-   [« lzf\_compress](function.lzf-compress.html)
    
-   [lzf\_optimized\_for »](function.lzf-optimized-for.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LZF](ref.lzf.html)
    
-   Розархівація LZF
    

# lzfdecompress

(PECL lzf >= 0.1.0)

lzfdecompress — Розархівація LZF

### Опис

```methodsynopsis
lzf_decompress(string $data): string
```

[lzf\_compress()](function.lzf-compress.html) розархівує рядок `data`, Що містить дані стиснуті алгоритмом lzf

### Список параметрів

`data`

Рядок зі стислими даними.

### Значення, що повертаються

Повертає розархівовані дані або **`false`** у разі виникнення помилки.

### Дивіться також

-   [lzf\_compress()](function.lzf-compress.html) - Стиснення LZF