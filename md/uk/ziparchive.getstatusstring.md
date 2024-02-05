---
navigation:
  - ziparchive.getnameindex.md: '« ZipArchive::getNameIndex'
  - ziparchive.getstream.md: 'ZipArchive::getStream »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::getStatusString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::getStatusString

(PHP 5 >= 5.2.7, PHP 7, PHP 8)

ZipArchive::getStatusString — Повертають статус повідомлення про помилку, системний та/або zip-статус

### Опис

```methodsynopsis
public ZipArchive::getStatusString(): string
```

Повертають статус повідомлення про помилку, системний та/або zip-статус.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string) із повідомленням про статус.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 / 1.18.0 | Метод можна викликати у закритому архіві. |
| 8.0.0 / 1.18.0 | Метод більше не повертає \*\*`false`\*\*в случае возникновения ошибки. |
