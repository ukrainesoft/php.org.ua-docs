---
navigation:
  - ziparchive.iscompressionmethoddupported.md: '« ZipArchive::isCompressionMethodSupported'
  - ziparchive.locatename.md: 'ZipArchive::locateName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::isEncryptionMethodSupported'
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

Метод шифрування, одна з констант **`ZipArchive::EM_*`**

`enc`

Якщо **`true`** перевірка шифрування, інакше перевірка розшифрування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише в тому випадку, якщо PHP зібрано з libzip ≥ 1.7.0.

### Дивіться також

-   [ZipArchive::setEncryptionIndex()](ziparchive.setencryptionindex.md) - Встановити метод шифрування запису за його індексом
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.md) - Встановити метод шифрування запису на його ім'я
