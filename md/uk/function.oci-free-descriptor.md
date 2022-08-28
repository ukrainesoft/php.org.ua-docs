Звільняє дескриптор

-   [« oci\_field\_type](function.oci-field-type.html)
    
-   [oci\_free\_statement »](function.oci-free-statement.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Звільняє дескриптор
    

# ocifreedescriptor

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifreedescriptor - Звільняє дескриптор

### Опис

```methodsynopsis
oci_free_descriptor(OCILob $lob): bool
```

Звільняє дескриптор, створений за допомогою [oci\_new\_descriptor()](function.oci-new-descriptor.html)

### Список параметрів

`descriptor`

Дескриптор, створений за допомогою [oci\_new\_descriptor()](function.oci-new-descriptor.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція зазвичай використовується як метод [OCILOB::free](ocilob.free.html)

### Дивіться також

-   [OCILOB::free](ocilob.free.html)