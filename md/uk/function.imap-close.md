Закрити потік IMAP

-   [« imapclearflagfull](function.imap-clearflag-full.html)
    
-   [imapcreate »](function.imap-create.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Закрити потік IMAP
    

# imapclose

(PHP 4, PHP 5, PHP 7, PHP 8)

imapclose — Закрити потік IMAP

### Опис

```methodsynopsis
imap_close(IMAP\Connection $imap, int $flags = 0): bool
```

Закриває IMAP-потік.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`flags`

Якщо встановлено **`CL_EXPUNGE`**, то ця функція мовчки застосує всі внесені зміни, зокрема видалить всі повідомлення, позначені для видалення. По суті зробить те саме, що і функція [imapexpunge()](function.imap-expunge.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imapopen()](function.imap-open.html) - Відкриває потік IMAP до поштової скриньки