---
navigation:
  - function.mailparse-msg-get-structure.md: « mailparse\_msg\_get\_structure
  - function.mailparse-msg-parse.md: mailparse\_msg\_parse »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparse\_msg\_parse\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mailparse\_msg\_parse\_file

(PECL mailparse >= 0.9.0)

mailparse\_msg\_parse\_file — Розібрати файл

### Опис

```methodsynopsis
mailparse_msg_parse_file(string $filename): resource
```

Розбирає файл. Це оптимальний шлях для аналізу файлу з поштовим повідомленням.

### Список параметрів

`filename`

Шлях до файлу. Файл буде відкритий та пропущений через аналізатор.

> **Зауваження** :
> 
> Повідомлення, що міститься в `filename`, має закінчуватися новим рядком (`CRLF`); інакше останній рядок повідомлення не буде проаналізовано.

### Значення, що повертаються

Повертає `MIME`\-ресурс, представляющий структуру, или\*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Рекомендується викликати [mailparse\_msg\_free()](function.mailparse-msg-free.md) для результату цієї функції, коли він більше не потрібен, щоб уникнути витоку пам'яті.

### Дивіться також

-   [mailparse\_msg\_free()](function.mailparse-msg-free.md) \- Вивільнити MIME-ресурс
-   [mailparse\_msg\_create()](function.mailparse-msg-create.md) \- Створює поштовий MIME-ресурс
