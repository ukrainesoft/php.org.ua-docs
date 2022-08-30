Повертає версію клієнтської бібліотеки

-   [« ocicancel](function.oci-cancel.html)
    
-   [ociclose »](function.oci-close.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Повертає версію клієнтської бібліотеки
    

# ociclientversion

(PHP 5> = 5.3.7, PHP 7, PHP 8, PECL OCI8> = 1.4.6)

ociclientversion — Повертає версію клієнтської бібліотеки

### Опис

```methodsynopsis
oci_client_version(): string
```

Повертає номер версії у вигляді рядка клієнтської C-бібліотеки Oracle, з якою пов'язаний PHP.

### Список параметрів

Немає.

### Значення, що повертаються

Повертає номер версії у вигляді рядка (string).

### Приклади

**Приклад #1 Приклад використання **ociclientversion()****

```php
<?php
    echo "Версия клиента: " . oci_client_version(); // Версия клиента: 19.9.0.0.0
?>
```

### Примітки

> **Зауваження**
> 
> Бібліотеки Oracle версій до 10*г*R2 немає необхідного функціоналу, щоб видати номер версії. У цьому випадку функція поверне рядок " Unknown " .

### Дивіться також

-   [ociserverversion()](function.oci-server-version.html) - Повертає версію сервера Oracle