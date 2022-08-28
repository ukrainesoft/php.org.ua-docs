Повертає останній номер помилки

-   [« fann\_get\_connection\_rate](function.fann-get-connection-rate.html)
    
-   [fann\_get\_errstr »](function.fann-get-errstr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає останній номер помилки
    

# fanngeterrno

(PECL fann> = 1.0.0)

fanngeterrno — Повертає останній номер помилки

### Опис

```methodsynopsis
fann_get_errno(resource $errdat): int
```

Повертає останній номер помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Номер помилки або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_reset\_errno()](function.fann-reset-errno.html) - скидає номер останньої помилки
-   [fann\_get\_errstr()](function.fann-get-errstr.html) - Повертає останній рядок помилки