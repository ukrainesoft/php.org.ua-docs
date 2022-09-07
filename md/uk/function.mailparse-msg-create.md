---
navigation:
  - function.mailparse-determine-best-xfer-encoding.md: « mailparsedeterminebestxferencoding
  - function.mailparse-msg-extract-part-file.md: mailparsemsgextractpartfile »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsemsgcreate
---
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
> Рекомендується викликати [mailparsemsgfree()](function.mailparse-msg-free.md) для результату цієї функції, коли він більше не потрібен, щоб уникнути витоку пам'яті.

### Дивіться також

-   [mailparsemsgfree()](function.mailparse-msg-free.md) - Вивільнити MIME-ресурс
-   [mailparsemsgparsefile()](function.mailparse-msg-parse-file.md) - Розібрати файл
