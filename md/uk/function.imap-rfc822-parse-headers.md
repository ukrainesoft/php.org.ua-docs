Розбір рядка заголовка листа

-   [« imap\_rfc822\_parse\_adrlist](function.imap-rfc822-parse-adrlist.html)
    
-   [imap\_rfc822\_write\_address »](function.imap-rfc822-write-address.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Розбір рядка заголовка листа
    

# imaprfc822parseheaders

(PHP 4, PHP 5, PHP 7, PHP 8)

imaprfc822parseheaders — Розбір рядка заголовка листа

### Опис

```methodsynopsis
imap_rfc822_parse_headers(string $headers, string $default_hostname = "UNKNOWN"): stdClass
```

Витягує об'єкт різних елементів заголовка, аналогічно [imap\_header()](function.imap-header.html)

### Список параметрів

`headers`

Дані для аналізу

`default_hostname`

Ім'я хоста за замовчуванням

### Значення, що повертаються

Повертає об'єкт, аналогічний функцією, що повертається [imap\_header()](function.imap-header.html), за винятком прапорів та інших властивостей, отриманих із сервера IMAP.

### Дивіться також

-   [imap\_rfc822\_parse\_adrlist()](function.imap-rfc822-parse-adrlist.html) - Розбір адресного рядка