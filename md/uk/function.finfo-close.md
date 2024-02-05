---
navigation:
  - function.finfo-buffer.md: « finfo\_buffer
  - function.finfo-file.md: finfo\_file »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функції модуля Fileinfo
title: finfo\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# finfo\_close

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfo\_close — Закриває екземпляр finfo

### Опис

```methodsynopsis
finfo_close(finfo $finfo): bool
```

Функція закриває екземпляр, який було відкрито функцією [finfo\_open()](function.finfo-open.md)

### Список параметрів

`finfo`

Екземпляр [finfo](class.finfo.md), що повертається функцією [finfo\_open()](function.finfo-open.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`finfo` тепер чекає екземпляр [finfo](class.finfo.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
