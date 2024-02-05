---
navigation:
  - function.mailparse-determine-best-xfer-encoding.md: « mailparse\_determine\_best\_xfer\_encoding
  - function.mailparse-msg-extract-part-file.md: mailparse\_msg\_extract\_part\_file »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparse\_msg\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mailparse\_msg\_create

(PECL mailparse >= 0.9.0)

mailparse\_msg\_create — Створює поштовий MIME-ресурс

### Опис

```methodsynopsis
mailparse_msg_create(): resource
```

Створює поштовий `MIME`\-ресурс.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає обробник, який можна використовувати для аналізу повідомлення.

### Примітки

> **Зауваження** :
> 
> Рекомендується викликати [mailparse\_msg\_free()](function.mailparse-msg-free.md) для результату цієї функції, коли він більше не потрібен, щоб уникнути витоку пам'яті.

### Дивіться також

-   [mailparse\_msg\_free()](function.mailparse-msg-free.md) \- Вивільнити MIME-ресурс
-   [mailparse\_msg\_parse\_file()](function.mailparse-msg-parse-file.md) \- Розібрати файл
