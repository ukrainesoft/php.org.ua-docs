Вивільнення ресурсу ключа

-   [« openssl\_error\_string](function.openssl-error-string.html)
    
-   [openssl\_get\_cert\_locations »](function.openssl-get-cert-locations.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Вивільнення ресурсу ключа
    

# opensslfreekey

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

opensslfreekey — Вивільнення ресурсу ключа

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
openssl_free_key(OpenSSLAsymmetricKey $key): void
```

**opensslfreekey()** видаляє ключ, пов'язаний із заданим ідентифікатором `key` із пам'яті.

### Список параметрів

`key`

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла, оскільки не має сенсу. |
|  | `key` тепер приймає [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html); раніше приймала ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` |