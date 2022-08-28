Розібрати файл

-   [« mailparse\_msg\_get\_structure](function.mailparse-msg-get-structure.html)
    
-   [mailparse\_msg\_parse »](function.mailparse-msg-parse.html)
    
-   [PHP Manual](index.html)
    
-   [Mailparse](ref.mailparse.html)
    
-   Розібрати файл
    

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
> Рекомендується викликати [mailparse\_msg\_free()](function.mailparse-msg-free.html) для результату цієї функції, коли він більше не потрібен, щоб уникнути витоку пам'яті.

### Дивіться також

-   [mailparse\_msg\_free()](function.mailparse-msg-free.html) - Вивільнити MIME-ресурс
-   [mailparse\_msg\_create()](function.mailparse-msg-create.html) - Створює поштовий MIME-ресурс