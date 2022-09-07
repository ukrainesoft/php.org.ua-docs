---
navigation:
  - function.imap-rfc822-parse-adrlist.md: « imaprfc822parseadrlist
  - function.imap-rfc822-write-address.md: imaprfc822writeaddress »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imaprfc822parseheaders
---
# imaprfc822parseheaders

(PHP 4, PHP 5, PHP 7, PHP 8)

imaprfc822parseheaders — Розбір рядка заголовка листа

### Опис

```methodsynopsis
imap_rfc822_parse_headers(string $headers, string $default_hostname = "UNKNOWN"): stdClass
```

Витягує об'єкт різних елементів заголовка, аналогічно [imapheader()](function.imap-header.md)

### Список параметрів

`headers`

Дані для аналізу

`default_hostname`

Ім'я хоста за замовчуванням

### Значення, що повертаються

Повертає об'єкт, аналогічний функцією, що повертається [imapheader()](function.imap-header.md), за винятком прапорів та інших властивостей, отриманих із сервера IMAP.

### Дивіться також

-   [imaprfc822parseadrlist()](function.imap-rfc822-parse-adrlist.md) - Розбір адресного рядка
