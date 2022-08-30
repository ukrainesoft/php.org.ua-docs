Повертає останній рядок помилки

-   [« fanngeterrno](function.fann-get-errno.html)
    
-   [fanngetlayerarray »](function.fann-get-layer-array.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає останній рядок помилки
    

# fanngeterrstr

(PECL fann> = 1.0.0)

fanngeterrstr — Повертає останній рядок помилки

### Опис

```methodsynopsis
fann_get_errstr(resource $errdat): string
```

Повертає останній рядок помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Останній рядок помилки або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannreseterrstr()](function.fann-reset-errstr.html) - Скидає останній рядок помилки
-   [fanngeterrno()](function.fann-get-errno.html) - Повертає останній номер помилки