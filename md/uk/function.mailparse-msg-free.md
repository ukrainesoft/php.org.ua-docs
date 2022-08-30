Вивільнити MIME-ресурс

-   [« mailparsemsgextractwholepartfile](function.mailparse-msg-extract-whole-part-file.html)
    
-   [mailparsemsggetpartdata »](function.mailparse-msg-get-part-data.html)
    
-   [PHP Manual](index.html)
    
-   [Mailparse](ref.mailparse.html)
    
-   Вивільнити MIME-ресурс
    

# mailparsemsgfree

(PECL mailparse >= 0.9.0)

mailparsemsgfree — Вивільнити MIME-ресурс

### Опис

```methodsynopsis
mailparse_msg_free(resource $mimemail): bool
```

Вивільняє `MIME`ресурс.

### Список параметрів

`mimemail`

Коректний `MIME`ресурс, створений [mailparsemsgcreate()](function.mailparse-msg-create.html) або [mailparsemsgparsefile()](function.mailparse-msg-parse-file.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mailparsemsgcreate()](function.mailparse-msg-create.html) - Створює поштовий MIME-ресурс
-   [mailparsemsgparsefile()](function.mailparse-msg-parse-file.html) - Розібрати файл