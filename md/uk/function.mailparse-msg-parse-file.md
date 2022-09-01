---
navigation:
  - function.mailparse-msg-get-structure.html: « mailparsemsggetstructure
  - function.mailparse-msg-parse.html: mailparsemsgparse »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsemsgparsefile
---
# mailparsemsgparsefile

(PECL mailparse >= 0.9.0)

mailparsemsgparsefile — Розібрати файл

### Опис

```methodsynopsis
mailparse_msg_parse_file(string $filename): resource
```

Розбирає файл. Це оптимальний шлях для аналізу файлу з поштовим повідомленням.

### Список параметрів

`filename`

Шлях до файлу. Файл буде відкритий та пропущений через аналізатор.

> **Зауваження**
> 
> Повідомлення, що міститься в `filename`, має закінчуватися новим рядком (`CRLF`); інакше останній рядок повідомлення не буде проаналізовано.

### Значення, що повертаються

Повертає `MIME`ресурс, що представляє структуру, або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Рекомендується викликати [mailparsemsgfree()](function.mailparse-msg-free.md) для результату цієї функції, коли він більше не потрібен, щоб уникнути витоку пам'яті.

### Дивіться також

-   [mailparsemsgfree()](function.mailparse-msg-free.md) - Вивільнити MIME-ресурс
-   [mailparsemsgcreate()](function.mailparse-msg-create.md) - Створює поштовий MIME-ресурс
