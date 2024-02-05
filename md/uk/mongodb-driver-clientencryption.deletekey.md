---
navigation:
  - mongodb-driver-clientencryption.decrypt.md: '« MongoDB\\Driver\\ClientEncryption::decrypt'
  - mongodb-driver-clientencryption.encrypt.md: 'MongoDB\\Driver\\ClientEncryption::encrypt »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::deleteKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::deleteKey

(mongodb >=1.15.0)

MongoDB\\Driver\\ClientEncryption::deleteKey — Видаляє документ із ключем

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::deleteKey(MongoDB\BSON\Binary $keyId): object
```

Видаляє документ із ключем із заданим UUID `keyId` колекції сховища ключів.

### Список параметрів

`keyId`

Екземпляр [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md) з підтипом 4 (UUID), що ідентифікує документ із ключем.

### Значення, що повертаються

Возвращает результат внутренней операции`deleteOne`над коллекцией хранилища ключей.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)у разі виникнення інших помилок.
