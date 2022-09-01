---
navigation:
  - ftp.resources.html: « Типи ресурсів
  - ftp.examples.html: Приклади »
  - index.html: PHP Manual
  - book.ftp.html: FTP
title: Обумовлені константи
---
# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`FTP_ASCII`** (int)

**`FTP_AUTOSEEK`** (int)

Дивіться опис функції [ftpsetoption()](function.ftp-set-option.md)

**`FTP_AUTORESUME`** (int)

Автоматичне визначення позиції старту та відновлення запитів PUT та GET (працює лише якщо дозволено FTPAUTOSEEK)

**`FTP_FAILED`** (int)

Асинхронна передача не вдалася.

**`FTP_FINISHED`** (int)

Асинхронна передача завершена.

**`FTP_MOREDATA`** (int)

Асинхронна передача ще активна.

**`FTP_TEXT`** (int)

Синонім для **`FTP_ASCII`**

**`FTP_BINARY`** (int)

**`FTP_IMAGE`** (int)

Синонім для **`FTP_BINARY`**

**`FTP_TIMEOUT_SEC`** (int)

Дивіться опис функції [ftpsetoption()](function.ftp-set-option.md)

**`FTP_USEPASVADDRESS`** (bool)

Дивіться опис функції [ftpsetoption()](function.ftp-set-option.md) для отримання інформації.
