---
navigation:
  - migration72.deprecated.md: '« Функціонал, оголошений застарілим у PHP 7.2.x'
  - migration71.md: Миграция с PHP 7.0.x на PHP 7.1.x »
  - index.md: PHP Manual
  - migration72.md: Миграция с PHP 7.1.x на PHP 7.2.x
title: Інші зміни
---
## Інші зміни

### Переміщення [utf8encode()](function.utf8-encode.md) і [utf8decode()](function.utf8-decode.md)

Функції [utf8encode()](function.utf8-encode.md) і [utf8decode()](function.utf8-decode.md) були переміщені в стандартну бібліотеку як функції роботи з рядками. У попередніх версіях для їх використання необхідно встановити модуль [XML](book.xml.md)

### Зміни [mail()](function.mail.md) і [мбsendmail()](function.mb-send-mail.md)

Параметр $additionalheaders функцій [mail()](function.mail.md) і [мбsendmail()](function.mb-send-mail.md) тепер приймає масив (array) замість рядка (string).

### Підтримка LMDB

Модуль [DBA](book.dba.md) отримав підтримку LMDB.

### Зміни в системі збирання PHP

-   Unix: Тепер для збирання PHP потрібно autoconf 2.64 або вище.
-   Unix: Для параметра конфігурації `--with-pdo-oci` більше не потрібно вказувати версію Oracle Instant Client.
-   Unix: Видалено параметр конфігурації `--enable-gd-native-ttf`. Він не використовувався з PHP 5.5.0.
-   Windows: Додано параметр конфігурації `--with-config-profile`. Він може бути використаний для збереження певних конфігурацій, таких як магічний файл config.nice.bat.

### Зміни в [ДД](book.image.md)

-   Тепер функція [imageantialias()](function.imageantialias.md) доступна при компіляції із системною бібліотекою libgd.
-   Функція [imagegd()](function.imagegd.md) зберігає truecolor-зображення як справжні truecolor-зображення. Раніше вони перетворювалися на зображення з фіксованою палітрою.

### Переміщення [MCrypt](book.mcrypt.md) у PECL

Модуль [MCrypt](book.mcrypt.md) був видалений з ядра PHP і переміщений PECL. Бібліотека mcrypt не оновлювалася з 2007 року і використовувати її не рекомендується. Замість неї використовуйте модуль [OpenSSL](book.openssl.md) або [Sodium](book.sodium.md)

### [sessionmodulename()](function.session-module-name.md)

Передача значення `"user"` в опцію [sessionmodulename()](function.session-module-name.md) тепер призведе до помилки рівня **`E_RECOVERABLE_ERROR`**. Раніше це просто ігнорувалося.
