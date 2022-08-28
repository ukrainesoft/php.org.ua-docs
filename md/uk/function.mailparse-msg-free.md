Вивільнити MIME-ресурс

-   [« mailparse\_msg\_extract\_whole\_part\_file](function.mailparse-msg-extract-whole-part-file.html)
    
-   [mailparse\_msg\_get\_part\_data »](function.mailparse-msg-get-part-data.html)
    
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

Коректний `MIME`ресурс, створений [mailparse\_msg\_create()](function.mailparse-msg-create.html) або [mailparse\_msg\_parse\_file()](function.mailparse-msg-parse-file.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mailparse\_msg\_create()](function.mailparse-msg-create.html) - Створює поштовий MIME-ресурс
-   [mailparse\_msg\_parse\_file()](function.mailparse-msg-parse-file.html) - Розібрати файл