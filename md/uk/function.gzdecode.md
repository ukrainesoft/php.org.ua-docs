Декодує рядок, стислий за допомогою gzip

-   [« gzcompress](function.gzcompress.html)
    
-   [gzdeflate »](function.gzdeflate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zlib](ref.zlib.html)
    
-   Декодує рядок, стислий за допомогою gzip
    

# gzdecode

(PHP 5> = 5.4.0, PHP 7, PHP 8)

gzdecode — Декодує рядок, стиснутий за допомогою gzip

### Опис

```methodsynopsis
gzdecode(string $data, int $max_length = 0): string|false
```

Ця функція повертає декодовану версію вхідних даних . `data`

### Список параметрів

`data`

Дані для декодування, закодовані за допомогою [gzencode()](function.gzencode.html)

`max_length`

Максимальний розмір рядка для декодування.

### Значення, що повертаються

Розпакований рядок або **`false`** у разі виникнення помилки.

### Помилки

У разі виникнення помилки повертає помилку рівня **`E_WARNING`**

### Дивіться також

-   [gzencode()](function.gzencode.html) - Створити стислий рядок gzip