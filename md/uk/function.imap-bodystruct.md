---
navigation:
  - function.imap-body.html: « imapbody
  - function.imap-check.html: imapcheck »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapbodystruct
---
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

Екземпляр [IMAPConnection](class.imap-connection.md)

`message_num`

Номер повідомлення

`section`

Секція тіла для читання

### Значення, що повертаються

Повертає інформацію у вигляді об'єкта або **`false`** у разі виникнення помилки. Опис структури та властивостей об'єкта читайте у розділі, присвяченому функції [imapfetchstructure()](function.imap-fetchstructure.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapfetchstructure()](function.imap-fetchstructure.md) - Прочитати структуру вказаного повідомлення
