Декодує рядок у MIME-заголовку

-   [« mb\_convert\_variables](function.mb-convert-variables.html)
    
-   [mb\_decode\_numericentity »](function.mb-decode-numericentity.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с многобайтовыми строками](ref.mbstring.html)
    
-   Декодує рядок у MIME-заголовку
    

# мбdecodemimeheader

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбdecodemimeheader — Декодує рядок у MIME-заголовку

### Опис

```methodsynopsis
mb_decode_mimeheader(string $string): string
```

Декодує закодований рядок (string) `string` у MIME-заголовку.

### Список параметрів

`string`

Рядок (string) для декодування.

### Значення, що повертаються

Декодований рядок (string) у внутрішньому кодуванні скрипта.

### Дивіться також

-   [mb\_encode\_mimeheader()](function.mb-encode-mimeheader.html) - Кодує рядок для MIME-заголовка