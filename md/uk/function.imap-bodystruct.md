Прочитати структуру вказаної секції тіла заданого повідомлення

-   [« imap\_body](function.imap-body.html)
    
-   [imap\_check »](function.imap-check.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Прочитати структуру вказаної секції тіла заданого повідомлення
    

# imapbodystruct

(PHP 4, PHP 5, PHP 7, PHP 8)

imapbodystruct — Прочитати структуру вказаної секції тіла заданого повідомлення

### Опис

```methodsynopsis
imap_bodystruct(IMAP\Connection $imap, int $message_num, string $section): stdClass|false
```

Читає структуру вказаної секції тіла заданого повідомлення.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`message_num`

Номер повідомлення

`section`

Секція тіла для читання

### Значення, що повертаються

Повертає інформацію у вигляді об'єкта або **`false`** у разі виникнення помилки. Опис структури та властивостей об'єкта читайте у розділі, присвяченому функції [imap\_fetchstructure()](function.imap-fetchstructure.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_fetchstructure()](function.imap-fetchstructure.html) - Прочитати структуру вказаного повідомлення