---
navigation:
  - migration72.deprecated.html: '« Функціонал, оголошений застарілим у PHP 7.2.x'
  - migration71.html: Миграция с PHP 7.0.x на PHP 7.1.x »
  - index.html: PHP Manual
  - migration72.html: Миграция с PHP 7.1.x на PHP 7.2.x
title: Інші зміни
---
## Інші зміни

### Переміщення [utf8encode()](function.utf8-encode.html) і [utf8decode()](function.utf8-decode.html)

Функції [utf8encode()](function.utf8-encode.html) і [utf8decode()](function.utf8-decode.html) були переміщені в стандартну бібліотеку як функції роботи з рядками. У попередніх версіях для їх використання необхідно встановити модуль [XML](book.xml.html)

### Зміни [mail()](function.mail.html) і [мбsendmail()](function.mb-send-mail.html)

Параметр $additionalheaders функцій [mail()](function.mail.html) і [мбsendmail()](function.mb-send-mail.html) тепер приймає масив (array) замість рядка (string).

### Підтримка LMDB

Модуль [DBA](book.dba.html) отримав підтримку LMDB.

### Зміни в системі збирання PHP

-   Unix: Тепер для збирання PHP потрібно autoconf 2.64 або вище.
-   Unix: Для параметра конфігурації `--with-pdo-oci` більше не потрібно вказувати версію Oracle Instant Client.
-   Unix: Видалено параметр конфігурації `--enable-gd-native-ttf`. Він не використовувався з PHP 5.5.0.
-   Windows: Додано параметр конфігурації `--with-config-profile`. Він може бути використаний для збереження певних конфігурацій, таких як магічний файл config.nice.bat.

### Зміни в [ДД](book.image.html)

-   Тепер функція [imageantialias()](function.imageantialias.html) доступна при компіляції із системною бібліотекою libgd.
-   Функція [imagegd()](function.imagegd.html) зберігає truecolor-зображення як справжні truecolor-зображення. Раніше вони перетворювалися на зображення з фіксованою палітрою.

### Переміщення [MCrypt](book.mcrypt.html) у PECL

Модуль [MCrypt](book.mcrypt.html) був видалений з ядра PHP і переміщений PECL. Бібліотека mcrypt не оновлювалася з 2007 року і використовувати її не рекомендується. Замість неї використовуйте модуль [OpenSSL](book.openssl.html) або [Sodium](book.sodium.html)

### [sessionmodulename()](function.session-module-name.html)

Передача значення `"user"` в опцію [sessionmodulename()](function.session-module-name.html) тепер призведе до помилки рівня **`E_RECOVERABLE_ERROR`**. Раніше це просто ігнорувалося.
