---
navigation:
  - function.imap-clearflag-full.md: « imap\_clearflag\_full
  - function.imap-create.md: imap\_create »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_close

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_close — Закриває потік IMAP

### Опис

```methodsynopsis
imap_close(IMAP\Connection $imap, int $flags = 0): true
```

Закриває IMAP-потік.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`flags`

Если установлен\*\*`CL_EXPUNGE`\*\*, то ця функція мовчки застосує всі внесені зміни, зокрема видалить всі повідомлення, позначені для видалення. По суті зробить те саме, що і функція [imap\_expunge()](function.imap-expunge.md)

### Значення, що повертаються

Функція завжди повертає **`true`**

### Помилки

Викидає виняток [ValueError](class.valueerror.md), если значение параметра`flags`недопустимо.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
| 8.0.0 | Тепер викидається виняток[ValueError](class.valueerror.md) при неприпустимих значеннях параметра `flags`. . Раніше виникало попередження та функція повертала логічне значення **`false`** |

### Дивіться також

-   [imap\_open()](function.imap-open.md) \- Відкриває потік IMAP до поштової скриньки
