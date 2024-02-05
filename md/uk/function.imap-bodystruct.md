---
navigation:
  - function.imap-body.md: « imap\_body
  - function.imap-check.md: imap\_check »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_bodystruct
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_bodystruct

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_bodystruct - Читає структуру зазначеної секції тіла заданого повідомлення

### Опис

```methodsynopsis
imap_bodystruct(IMAP\Connection $imap, int $message_num, string $section): stdClass|false
```

Читає структуру вказаної секції тіла заданого повідомлення.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_num`

Номер повідомлення

`section`

Секція тіла для читання

### Значення, що повертаються

Повертає інформацію у вигляді об'єкта або **`false`** у разі виникнення помилки. Опис структури та властивостей об'єкта читайте у розділі, присвяченому функції [imap\_fetchstructure()](function.imap-fetchstructure.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_fetchstructure()](function.imap-fetchstructure.md) \- Читає структуру вказаного повідомлення
