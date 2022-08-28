Інші зміни у модулях

-   [« Изменения OpenSSL в PHP 5.6.x](migration56.openssl.html)
    
-   [Новые глобальные константы »](migration56.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 5.5.x на PHP 5.6.x](migration56.html)
    
-   Інші зміни у модулях
    

## Інші зміни у модулях

### [cURL](book.curl.html)

Ряд констант, помічені як застарілі в бібліотеці cURL, будуть видалені:

-   **`CURLOPT_CLOSEPOLICY`**
-   **`CURLCLOSEPOLICY_CALLBACK`**
-   **`CURLCLOSEPOLICY_LEAST_RECENTLY_USED`**
-   **`CURLCLOSEPOLICY_LEAST_TRAFFIC`**
-   **`CURLCLOSEPOLICY_OLDEST`**
-   **`CURLCLOSEPOLICY_SLOWEST`**

### [OCI8](book.oci8.html)

-   Підтримка неявних наборів результатів для Oracle Database 12c була додана за допомогою нової функції [oci\_get\_implicit\_resultset()](function.oci-get-implicit-resultset.html)
-   За допомогою `oci_execute($s, OCI_NO_AUTO_COMMIT)`для SELECT більше необов'язково ініціювати внутрішній ROLLBACK під час закриття з'єднання.
-   Додані зонди DTrace, що контролюються за допомогою опції конфігурації `--enable-dtrace`
-   [oci\_internal\_debug()](function.oci-internal-debug.html) тепер нічого не робить.
-   Формат виведення функції [phpinfo()](function.phpinfo.html) для OCI8 змінилося.

### [Zip](book.zip.html)

Додана опція конфігурації `--with-libzip`для використання системної бібліотеки libzip. Потрібно щонайменше libzip версії 0.11, рекомендується 0.11.2 або пізніша.

### [MySQLi](book.mysqli.html)

Додано опцію [mysqli.rollback\_on\_cached\_plink](mysqli.configuration.html#ini.mysqli.rollback-on-cached-plink)яка управляє поведінкою відкату постійних з'єднань.