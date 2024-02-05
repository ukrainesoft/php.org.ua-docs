---
navigation:
  - mongodb-driver-clientencryption.getkeybyaltname.md: '« MongoDB\\Driver\\ClientEncryption::getKeyByAltName'
  - mongodb-driver-clientencryption.removekeyaltname.md: 'MongoDB\\Driver\\ClientEncryption::removeKeyAltName »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::getKeys'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::getKeys

(mongodb >=1.15.0)

MongoDB\\Driver\\ClientEncryption::getKeys — Отримує всі документи з ключем

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::getKeys(): MongoDB\Driver\Cursor
```

Знаходить усі документи з ключем у колекції сховища ключів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)у разі виникнення інших помилок.
