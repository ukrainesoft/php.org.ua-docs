---
navigation:
  - mongodb-driver-clientencryption.createdatakey.md: '« MongoDBDriverClientEncryption::createDataKey'
  - mongodb-driver-clientencryption.encrypt.md: 'MongoDBDriverClientEncryption::encrypt »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDBDriverClientEncryption
title: 'MongoDBDriverClientEncryption::decrypt'
---
# MongoDBDriverClientEncryption::decrypt

(mongodb >=1.7.0)

MongoDBDriverClientEncryption::decrypt — Розшифрувати дані

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::decrypt(MongoDB\BSON\Binary $value): mixed
```

Розшифровує значення.

### Список параметрів

`value`

Об'єкт класу [MongoDBBSONBinary](class.mongodb-bson-binary.md) з підтипом 6, що містить зашифровані дані.

### Значення, що повертаються

Повертає розшифровані дані у тому вигляді, як вони були передані в [MongoDBDriverClientEncryption::encrypt()](mongodb-driver-clientencryption.encrypt.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDBDriverExceptionEncryptionException](class.mongodb-driver-exception-encryptionexception.md) якщо в процесі дешифрування сталася помилка

### Дивіться також

-   [MongoDBDriverClientEncryption::encrypt()](mongodb-driver-clientencryption.encrypt.md) - Шифрує дані
