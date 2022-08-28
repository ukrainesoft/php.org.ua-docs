Повертає опис помилки для коду помилки FDF

-   [« fdf\_errno](function.fdf-errno.html)
    
-   [fdf\_get\_ap »](function.fdf-get-ap.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Повертає опис помилки для коду помилки FDF
    

# fdferror

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdferror — Повертає опис помилки для коду помилки FDF

### Опис

```methodsynopsis
fdf_error(int $error_code = -1): string
```

Отримує текстовий опис коду помилки FDF, зазначеного в `error_code`

### Список параметрів

`error_code`

Код помилки, отриманий за допомогою [fdf\_errno()](function.fdf-errno.html). Якщо не вказано, функція використовує код внутрішньої помилки, встановлений останньою операцією.

### Значення, що повертаються

Повертає повідомлення про помилку у вигляді рядка або рядка `no error`якщо помилки немає.

### Дивіться також

-   [fdf\_errno()](function.fdf-errno.html) - Повертає код помилки для останньої операції FDF