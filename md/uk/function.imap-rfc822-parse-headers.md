---
navigation:
  - function.imap-rfc822-parse-adrlist.md: « imap\_rfc822\_parse\_adrlist
  - function.imap-rfc822-write-address.md: imap\_rfc822\_write\_address »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_rfc822\_parse\_headers
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_rfc822\_parse\_headers

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_rfc822\_parse\_headers — Розбирає рядок заголовка листа

### Опис

```methodsynopsis
imap_rfc822_parse_headers(string $headers, string $default_hostname = "UNKNOWN"): stdClass
```

Витягує об'єкт різних елементів заголовка, аналогічно функції [imap\_header()](function.imap-header.md)

### Список параметрів

`headers`

Дані для аналізу

`default_hostname`

Ім'я хоста за замовчуванням

### Значення, що повертаються

Повертає об'єкт, аналогічний функцією, що повертається [imap\_header()](function.imap-header.md), за винятком прапорів та інших властивостей, отриманих із сервера IMAP.

### Дивіться також

-   [imap\_rfc822\_parse\_adrlist()](function.imap-rfc822-parse-adrlist.md) \- Розбирає адресний рядок
