---
navigation:
  - migration56.openssl.md: « Зміни OpenSSL в PHP 5.6.x
  - migration56.constants.md: Нові глобальні константи »
  - index.md: PHP Manual
  - migration56.md: Міграція з PHP 5.5.x на PHP 5.6.x
title: Інші зміни у модулях
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   Підтримка неявних наборів результатів для Oracle Database 12c була додана за допомогою нової функції[oci\_get\_implicit\_resultset()](function.oci-get-implicit-resultset.md)
-   За допомогою`oci_execute($s, OCI_NO_AUTO_COMMIT)`для SELECT більше необов'язково ініціювати внутрішній ROLLBACK під час закриття з'єднання.
-   Додані зонди DTrace, що контролюються за допомогою опції конфігурації`--enable-dtrace`
-   [oci\_internal\_debug()](function.oci-internal-debug.md)тепер нічого не робить.
-   Формат виведення функції[phpinfo()](function.phpinfo.md)для OCI8 змінилося.

### [Zip](book.zip.md)

Добавлена опция конфигурации`--with-libzip`для використання системної бібліотеки libzip. Потрібно щонайменше libzip версії 0.11, рекомендується 0.11.2 або пізніша.

### [MySQLi](book.mysqli.md)

Додано опцію [mysqli.rollback\_on\_cached\_plink](mysqli.configuration.md#ini.mysqli.rollback-on-cached-plink)яка управляє поведінкою відкату постійних з'єднань.
