---
navigation:
  - ziparchive.setencryptionindex.md: '« ZipArchive::setEncryptionIndex'
  - ziparchive.setexternalattributesindex.md: 'ZipArchive::setExternalAttributesIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setEncryptionName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::setEncryptionName

(PHP >= 7.2.0, PHP 8, PECL zip >= 1.14.0)

ZipArchive::setEncryptionName — Встановити метод шифрування запису на його ім'я

### Опис

```methodsynopsis
public ZipArchive::setEncryptionName(string $name, int $method, ?string $password = null): bool
```

Встановити метод шифрування запису, вказаного на його ім'я.

### Список параметрів

`name`

Назва запису.

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

### Приклади

У цьому прикладі створюється ZIP-архів test.zip, який містить файл test.txt, зашифрований за допомогою AES 256.

**Приклад #1 Архівуємо та шифруємо файл**

```php
<?php
$zip = new ZipArchive();
if ($zip->open('test.zip', ZipArchive::CREATE) === TRUE) {
    $zip->setPassword('secret');
    $zip->addFile('text.txt');
    $zip->setEncryptionName('text.txt', ZipArchive::EM_AES_256);
    $zip->close();
    echo "готово\n";
} else {
    echo "ошибка\n";
}
?>
```

### Примітки

> **Зауваження** :
> 
> Функція доступна лише якщо скомпільовано за допомогою libzip ≥ 1.2.0.

### Дивіться також

-   [ZipArchive::setPassword()](ziparchive.setpassword.md) \- Встановлення пароля для активного архіву
-   [ZipArchive::setEncryptionIndex()](ziparchive.setencryptionindex.md) \- Встановити метод шифрування запису за його індексом
