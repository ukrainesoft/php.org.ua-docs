---
navigation:
  - function.imap-uid.md: « imap\_uid
  - function.imap-unsubscribe.md: imap\_unsubscribe »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_undelete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_undelete

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_undelete — Знімає з повідомлення позначку видалення

### Опис

```methodsynopsis
imap_undelete(IMAP\Connection $imap, string $message_nums, int $flags = 0): true
```

Видаляє із заданого повідомлення мітку видалення, яка була встановлена ​​за допомогою [imap\_delete()](function.imap-delete.md) або [imap\_mail\_move()](function.imap-mail-move.md)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_nums`

Рядок (string), що складається з одного або декількох повідомлень у форматі послідовності у стилі IMAP4 (`"n"` `"n:m"` або їх комбінація, розділена комами).

`flags`

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_delete()](function.imap-delete.md) \- Позначає повідомлення для видалення
-   [imap\_mail\_move()](function.imap-mail-move.md) \- Переміщує вказані повідомлення у вказану поштову скриньку
