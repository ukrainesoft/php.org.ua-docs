---
navigation:
  - mongodb-driver-clientencryption.createdatakey.md: '« MongoDB\\Driver\\ClientEncryption::createDataKey'
  - mongodb-driver-clientencryption.deletekey.md: 'MongoDB\\Driver\\ClientEncryption::deleteKey »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::decrypt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::decrypt

(mongodb >=1.7.0)

MongoDB\\Driver\\ClientEncryption::decrypt — Розшифрувати дані

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::decrypt(MongoDB\BSON\Binary $value): mixed
```

Розшифровує значення.

### Список параметрів

`value`

Об'єкт класу [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md) з підтипом 6, що містить зашифровані дані.

### Значення, що повертаються

Повертає розшифровані дані у тому вигляді, як вони були передані в [MongoDB\\Driver\\ClientEncryption::encrypt()](mongodb-driver-clientencryption.encrypt.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDB\\Driver\\Exception\\EncryptionException](class.mongodb-driver-exception-encryptionexception.md)якщо в процесі дешифрування сталася помилка

### Дивіться також

-   [MongoDB\\Driver\\ClientEncryption::encrypt()](mongodb-driver-clientencryption.encrypt.md) \- Шифрує дані
