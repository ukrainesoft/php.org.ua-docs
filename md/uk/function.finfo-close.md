---
navigation:
  - function.finfo-buffer.md: « finfobuffer
  - function.finfo-file.md: finfofile »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функции модуля Fileinfo
title: finfoclose
---
# finfoclose

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfoclose — Закриває екземпляр finfo

### Опис

```methodsynopsis
finfo_close(finfo $finfo): bool
```

Функція закриває екземпляр, який було відкрито функцією [finfoopen()](function.finfo-open.md)

### Список параметрів

`finfo`

Екземпляр [finfo](class.finfo.md), що повертається функцією [finfoopen()](function.finfo-open.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `finfo` тепер чекає екземпляр [finfo](class.finfo.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
