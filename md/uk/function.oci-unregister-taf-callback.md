Видалити реєстрацію користувача callback-функції для Oracle Database TAF

-   [« oci\_statement\_type](function.oci-statement-type.html)
    
-   [OCICollection »](class.ocicollection.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Видалити реєстрацію користувача callback-функції для Oracle Database TAF
    

# ociunregistertafcallback

(PHP 7.0 >= 7.0.23, PHP 8, PHP 7 >= 7.1.9, PHP 8, PECL OCI8 >= 2.1.7)

ociunregistertafcallback — Видалити реєстрацію користувача callback-функції для Oracle Database TAF

### Опис

```methodsynopsis
oci_unregister_taf_callback(resource $connection): bool
```

Видаляє реєстрацію користувача callback-функції, зареєстровану для з'єднання `connection` за допомогою [oci\_register\_taf\_callback()](function.oci-register-taf-callback.html). Детальніше читайте [OCI8 Transparent Application Failover (TAF) Support](oci8.taf.html)

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [oci\_register\_taf\_callback()](function.oci-register-taf-callback.html) - Реєструє функцію зворотного виклику для Oracle Database TAF