---
navigation:
  - mongodb-driver-clientencryption.encryptexpression.md: '« MongoDB\\Driver\\ClientEncryption::encryptExpression'
  - mongodb-driver-clientencryption.getkeybyaltname.md: 'MongoDB\\Driver\\ClientEncryption::getKeyByAltName »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::getKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::getKey

(mongodb >=1.15.0)

MongoDB\\Driver\\ClientEncryption::getKey — Отримує документ із ключем

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::getKey(MongoDB\BSON\Binary $keyId): ?object
```

Знаходить єдиний документ із ключем у колекції сховища ключів із заданим UUID `keyId`

### Список параметрів

`keyId`

Екземпляр [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md) з підтипом 4 (UUID), що ідентифікує документ із ключем.

### Значення, що повертаються

Повертає документ із ключем або **`null`**, якщо жоден документ не збігся.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)у разі виникнення інших помилок.
