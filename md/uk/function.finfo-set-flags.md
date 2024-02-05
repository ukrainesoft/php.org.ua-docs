---
navigation:
  - function.finfo-open.md: « finfo\_open
  - function.mime-content-type.md: mime\_content\_type »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функції модуля Fileinfo
title: finfo\_set\_flags
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# finfo\_set\_flags

# finfo::set\_flags

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfo\_set\_flags -- finfo::set\_flags — Встановлює параметри конфігурації libmagic

### Опис

Процедурний стиль

```methodsynopsis
finfo_set_flags(finfo $finfo, int $flags): bool
```

Об'єктно-орієнтований стиль

```methodsynopsis
public finfo::set_flags(int $flags): bool
```

Функція встановлює різні параметри FileInfo. Опції також можуть бути встановлені безпосередньо в [finfo\_open()](function.finfo-open.md) або інших функцій Fileinfo.

### Список параметрів

`finfo`

Екземпляр [finfo](class.finfo.md), що повертається функцією [finfo\_open()](function.finfo-open.md)

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`finfo` тепер чекає екземпляр [finfo](class.finfo.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
