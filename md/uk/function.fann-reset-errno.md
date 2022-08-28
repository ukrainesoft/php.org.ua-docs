Скидає номер останньої помилки

-   [« fann\_read\_train\_from\_file](function.fann-read-train-from-file.html)
    
-   [fann\_reset\_errstr »](function.fann-reset-errstr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Скидає номер останньої помилки
    

# fannreseterrno

(PECL fann> = 1.0.0)

fannreseterrno — Скидає номер останньої помилки

### Опис

```methodsynopsis
fann_reset_errno(resource $errdat): void
```

Скидає номер останньої помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Не повертає жодного значення.

### Дивіться також

-   [fann\_get\_errno()](function.fann-get-errno.html) - Повертає останній номер помилки
-   [fann\_reset\_errstr()](function.fann-reset-errstr.html) - Скидає останній рядок помилки