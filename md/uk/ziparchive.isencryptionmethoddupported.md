---
navigation:
  - ziparchive.iscompressionmethoddupported.md: '« ZipArchive::isCompressionMethodSupported'
  - ziparchive.locatename.md: 'ZipArchive::locateName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::isEncryptionMethodSupported'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::isEncryptionMethodSupported

(PHP >= 8.0.0, PECL zip >= 1.19.0)

ZipArchive::isEncryptionMethodSupported — Перевіряє, чи підтримується метод шифрування libzip

### Опис

```methodsynopsis
public static ZipArchive::isEncryptionMethodSupported(int $method, bool $enc = true): bool
```

Перевіряє, чи підтримується метод шифрування libzip.

### Список параметрів

`method`

Метод шифрования, одна из констант\*\*`ZipArchive::EM_*`\*\*

`enc`

Якщо \*\*`true`\*\*проверка шифрования, иначе проверка расшифровки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише в тому випадку, якщо PHP зібрано з libzip ≥ 1.7.0.

### Дивіться також

-   [ZipArchive::setEncryptionIndex()](ziparchive.setencryptionindex.md) \- Встановити метод шифрування запису за його індексом
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.md) \- Встановити метод шифрування запису на його ім'я
