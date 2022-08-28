Створює поштовий MIME-ресурс

-   [« mailparse\_determine\_best\_xfer\_encoding](function.mailparse-determine-best-xfer-encoding.html)
    
-   [mailparse\_msg\_extract\_part\_file »](function.mailparse-msg-extract-part-file.html)
    
-   [PHP Manual](index.html)
    
-   [Mailparse](ref.mailparse.html)
    
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
> Рекомендується викликати [mailparse\_msg\_free()](function.mailparse-msg-free.html) для результату цієї функції, коли він більше не потрібен, щоб уникнути витоку пам'яті.

### Дивіться також

-   [mailparse\_msg\_free()](function.mailparse-msg-free.html) - Вивільнити MIME-ресурс
-   [mailparse\_msg\_parse\_file()](function.mailparse-msg-parse-file.html) - Розібрати файл