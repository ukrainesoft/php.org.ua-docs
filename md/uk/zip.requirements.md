---
navigation:
  - zip.setup.md: « Встановлення та налаштування
  - zip.installation.md: Установка »
  - index.md: PHP Manual
  - zip.setup.md: Встановлення та налаштування
title: Вимоги
---
## Вимоги

Для модуля потрібно [» libzip](https://libzip.org/). Версія 1.1.2 була включена до PHP до версії 7.3.

Мінімальна підтримувана версія — 0.11, але рекомендується використовувати вищу версію.

-   Для підтримки шифрування потрібна версія 1.2, дивіться [ZipArchive::setEncryptionIndex()](ziparchive.setencryptionindex.md)
-   Для підтримки прогресу потрібна версія 1.3, дивіться [ZipArchive::registerProgressCallback()](ziparchive.registerprogresscallback.md)
-   Для підтримки скасування потрібна версія 1.6, дивіться [ZipArchive::registerCancelCallback()](ziparchive.registercancelcallback.md)
