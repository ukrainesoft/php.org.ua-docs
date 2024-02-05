---
navigation:
  - ziparchive.setcompressionname.md: '« ZipArchive::setCompressionName'
  - ziparchive.setencryptionname.md: 'ZipArchive::setEncryptionName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setEncryptionIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::setEncryptionIndex

(PHP >= 7.2.0, PHP 8, PECL zip >= 1.14.0)

ZipArchive::setEncryptionIndex — Встановити метод шифрування запису за його індексом

### Опис

```methodsynopsis
public ZipArchive::setEncryptionIndex(int $index, int $method, ?string $password = null): bool
```

Встановлює метод шифрування запису, вказаного за індексом.

### Список параметрів

`index`

Індекс запису.

`method`

Метод шифрування, заданий однією із констант ZipArchive::EM\_

`password`

Пароль. Якщо не вказувати, буде використано пароль за замовчуванням.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `password` тепер допускає значення null. |

### Примітки

> **Зауваження** :
> 
> Функція доступна лише якщо скомпільовано за допомогою libzip ≥ 1.2.0.

### Дивіться також

-   [ZipArchive::setPassword()](ziparchive.setpassword.md) \- Встановлення пароля для активного архіву
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.md) \- Встановити метод шифрування запису на його ім'я
