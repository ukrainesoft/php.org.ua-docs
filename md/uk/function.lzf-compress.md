Стиснення LZF

-   [« Функции LZF](ref.lzf.html)
    
-   [lzf\_decompress »](function.lzf-decompress.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LZF](ref.lzf.html)
    
-   Стиснення LZF
    

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

-   [lzf\_decompress()](function.lzf-decompress.html) - Розархівація LZF