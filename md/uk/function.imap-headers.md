---
navigation:
  - function.imap-headerinfo.md: « imap\_headerinfo
  - function.imap-is-open.md: imap\_is\_open »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_headers
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_headers

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_headers — Отримує заголовки всіх повідомлень у поштовій скриньці

### Опис

```methodsynopsis
imap_headers(IMAP\Connection $imap): array|false
```

Повертає заголовки всіх повідомлень у поштовій скриньці.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

### Значення, що повертаються

Повертає масив із рядками, що містять заголовки повідомлень. Один елемент – одне повідомлення. Повертає \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
