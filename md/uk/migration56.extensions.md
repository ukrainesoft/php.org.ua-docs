---
navigation:
  - migration56.openssl.md: « Изменения OpenSSL в PHP 5.6.x
  - migration56.constants.md: Нові глобальні константи »
  - index.md: PHP Manual
  - migration56.md: Миграция с PHP 5.5.x на PHP 5.6.x
title: Інші зміни у модулях
---
## Інші зміни у модулях

### [cURL](book.curl.md)

Ряд констант, помічені як застарілі в бібліотеці cURL, будуть видалені:

-   **`CURLOPT_CLOSEPOLICY`**
-   **`CURLCLOSEPOLICY_CALLBACK`**
-   **`CURLCLOSEPOLICY_LEAST_RECENTLY_USED`**
-   **`CURLCLOSEPOLICY_LEAST_TRAFFIC`**
-   **`CURLCLOSEPOLICY_OLDEST`**
-   **`CURLCLOSEPOLICY_SLOWEST`**

### [OCI8](book.oci8.md)

-   Підтримка неявних наборів результатів для Oracle Database 12c була додана за допомогою нової функції [ocigetimplicitresultset()](function.oci-get-implicit-resultset.html)
-   За допомогою `oci_execute($s, OCI_NO_AUTO_COMMIT)`для SELECT більше необов'язково ініціювати внутрішній ROLLBACK під час закриття з'єднання.
-   Додані зонди DTrace, що контролюються за допомогою опції конфігурації `--enable-dtrace`
-   [ociinternaldebug()](function.oci-internal-debug.html) тепер нічого не робить.
-   Формат виведення функції [phpinfo()](function.phpinfo.md) для OCI8 змінилося.

### [Zip](book.zip.md)

Додана опція конфігурації `--with-libzip`для використання системної бібліотеки libzip. Потрібно щонайменше libzip версії 0.11, рекомендується 0.11.2 або пізніша.

### [MySQLi](book.mysqli.md)

Додано опцію [mysqli.rollbackвінcachedplink](mysqli.configuration.html#ini.mysqli.rollback-on-cached-plink)яка управляє поведінкою відкату постійних з'єднань.
