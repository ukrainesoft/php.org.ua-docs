Закінчує процес читання з курсору

-   [« oci\_bind\_by\_name](function.oci-bind-by-name.html)
    
-   [oci\_client\_version »](function.oci-client-version.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Закінчує процес читання з курсору
    

# ocicancel

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocicancel — Закінчує процес читання з курсору

### Опис

```methodsynopsis
oci_cancel(resource $statement): bool
```

Скидає курсор, звільняючи всі пов'язані ресурси та скасовує можливість читати з нього.

### Список параметрів

`statement`

Запит OCI.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.