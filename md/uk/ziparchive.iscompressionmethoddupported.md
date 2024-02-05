---
navigation:
  - ziparchive.getstreamname.md: '« ZipArchive::getStreamName'
  - ziparchive.isencryptionmethoddupported.md: 'ZipArchive::isEncryptionMethodSupported »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::isCompressionMethodSupported'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::isCompressionMethodSupported

(PHP >= 8.0.0, PECL zip >= 1.19.0)

ZipArchive::isCompressionMethodSupported — Перевіряє, чи підтримується метод стиснення libzip

### Опис

```methodsynopsis
public static ZipArchive::isCompressionMethodSupported(int $method, bool $enc = true): bool
```

Перевіряє, чи підтримується метод стиснення libzip.

### Список параметрів

`method`

Метод сжатия, одна из констант\*\*`ZipArchive::CM_*`\*\*

`enc`

Якщо \*\*`true`\*\*проверка на сжатие, иначе проверка на декомпрессию.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише в тому випадку, якщо PHP зібрано з libzip ≥ 1.7.0.

### Дивіться також

-   [ZipArchive::setCompressionIndex()](ziparchive.setcompressionindex.md) \- Встановити метод стиснення запису, заданого його індексом
-   [ZipArchive::setCompressionName()](ziparchive.setcompressionname.md) \- Встановити метод стиснення запису, заданого на ім'я
