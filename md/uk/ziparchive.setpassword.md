---
navigation:
  - ziparchive.setmtimename.md: '« ZipArchive::setMtimeName'
  - ziparchive.statindex.md: 'ZipArchive::statIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setPassword'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::setPassword

(PHP 5 >= 5.6.0, PHP 7, PHP 8, PECL zip >= 1.12.4)

ZipArchive::setPassword — Встановлення пароля для активного архіву

### Опис

```methodsynopsis
public ZipArchive::setPassword(string $password): bool
```

Вказує пароль для активного архіву.

### Список параметрів

`password`

Пароль для архіву.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Починаючи з PHP 7.2.0 і libzip 1.2.0, пароль використовується для розпакування архіву, а також як пароль за замовчуванням для [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.md) і [ZipArchive::setEncryptionIndex()](ziparchive.setencryptionindex.md). Раніше ця функція встановлювала пароль лише для розпакування. Вона не перетворювала не захищений паролем [ZipArchive](class.ziparchive.md) у захищений [ZipArchive](class.ziparchive.md)

### Дивіться також

-   [ZipArchive::setEncryptionIndex()](ziparchive.setencryptionindex.md) \- Встановити метод шифрування запису за його індексом
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.md) \- Встановити метод шифрування запису на його ім'я
