---
navigation:
  - migration74.other-changes.html: « Другие изменения
  - migration73.md: Миграция с PHP 7.2.x на PHP 7.3.x »
  - index.md: PHP Manual
  - migration74.md: Миграция с PHP 7.3.x на PHP 7.4.x
title: Підтримка Windows
---
## Підтримка Windows

### Прапори **configure**

**configure** тепер враховує додаткові змінні оточення `CFLAGS` і `LDFLAGS`

### Обробка CTRL

Комбінації клавіш CTRL+C та CTRL+BREAK у командному рядку можна перехопити, встановивши функцію-обробник за допомогою [sapiwindowssetctrlhandler()](function.sapi-windows-set-ctrl-handler.html)

Функції [procopen()](function.proc-open.html) на Windows може бути передана опція "createprocessgroup". Це потрібно, якщо дочірній процес має обробляти події CTRL.

### OPcache

OPcache тепер підтримує довільну кількість окремих кешів на кожного користувача за допомогою INI-директиви `opcache.cache_id`. Всі процеси з однаковим ідентифікатором кешу та користувачем використовують один і той самий екземпляр OPcache.

### стати

Поліпшено реалізацію stat.

-   Передається номер індексного дескриптора (inode), який спирається на індекс файлу NTFS.
-   Номер пристрою тепер виходить із серійного номера тома.

Зверніть увагу, що на 64-бітових системах обидва значення витягуються із системи у вихідному вигляді. У 32-розрядних системах ці значення фіктивні, тому що можуть перевищувати максимальне 32-розрядне ціле число, дозволене PHP.

### libsqlite3

libsqlite3 більше не компілюється статично у phpsqlite3.dll та phppdosqlite.dll, але доступний як libsqlite3.dll. Зверніться до інструкції з установки для [SQLite3](sqlite3.installation.md) і [PDOSQLITE](ref.pdo-sqlite.html#ref.pdo-sqlite.installation) відповідно.
