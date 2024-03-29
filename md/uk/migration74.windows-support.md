---
navigation:
  - migration74.other-changes.md: « Інші зміни
  - migration73.md: Міграція з PHP 7.2.x на PHP 7.3.x »
  - index.md: PHP Manual
  - migration74.md: Міграція з PHP 7.3.x на PHP 7.4.x
title: Підтримка Windows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Підтримка Windows

### Флаги**configure**

**configure** тепер враховує додаткові змінні оточення `CFLAGS`и`LDFLAGS`

### Обробка CTRL

Комбінації клавіш CTRL+C та CTRL+BREAK у командному рядку можна перехопити, встановивши функцію-обробник за допомогою [sapi\_windows\_set\_ctrl\_handler()](function.sapi-windows-set-ctrl-handler.md)

Функції [proc\_open()](function.proc-open.md) на Windows може бути передана опція "create\_process\_group". Це потрібно, якщо дочірній процес має обробляти події CTRL.

### OPcache

OPcache тепер підтримує довільну кількість окремих кешів на кожного користувача за допомогою INI-директиви `opcache.cache_id`. Всі процеси з однаковим ідентифікатором кеша та користувачем використовують один і той самий екземпляр OPcache.

### stat

Поліпшено реалізацію stat.

-   Передається номер індексного дескриптора (inode), який спирається на індекс файлу NTFS.
-   Номер пристрою тепер виходить із серійного номера тома.

Зверніть увагу, що на 64-бітових системах обидва значення витягуються із системи у вихідному вигляді. У 32-розрядних системах ці значення фіктивні, тому що можуть перевищувати максимальне 32-розрядне ціле число, дозволене PHP.

### libsqlite3

libsqlite3 більше не компілюється статично у php\_sqlite3.dll та php\_pdo\_sqlite.dll, но доступен как libsqlite3.dll. Обратитесь к инструкции по установке для[SQLite3](sqlite3.installation.md) і [PDO\_SQLITE](ref.pdo-sqlite.md#ref.pdo-sqlite.installation)соответственно.
