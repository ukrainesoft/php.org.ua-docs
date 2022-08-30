Створює поштовий MIME-ресурс

-   [« mailparsedeterminebestxferencoding](function.mailparse-determine-best-xfer-encoding.html)
    
-   [mailparsemsgextractpartfile »](function.mailparse-msg-extract-part-file.html)
    
-   [PHP Manual](index.md)
    
-   [Mailparse](ref.mailparse.md)
    
-   Створює поштовий MIME-ресурс
    

# mailparsemsgcreate

(PECL mailparse >= 0.9.0)

mailparsemsgcreate — Створює поштовий MIME-ресурс

### Опис

```methodsynopsis
mailparse_msg_create(): resource
```

Створює поштовий `MIME`ресурс.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає обробник, який можна використовувати для аналізу повідомлення.

### Примітки

> **Зауваження**
> 
> Рекомендується викликати [mailparsemsgfree()](function.mailparse-msg-free.html) для результату цієї функції, коли він більше не потрібен, щоб уникнути витоку пам'яті.

### Дивіться також

-   [mailparsemsgfree()](function.mailparse-msg-free.html) - Вивільнити MIME-ресурс
-   [mailparsemsgparsefile()](function.mailparse-msg-parse-file.html) - Розібрати файл