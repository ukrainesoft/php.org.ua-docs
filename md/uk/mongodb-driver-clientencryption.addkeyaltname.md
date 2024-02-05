---
navigation:
  - class.mongodb-driver-clientencryption.md: « MongoDB\\Driver\\ClientEncryption
  - mongodb-driver-clientencryption.construct.md: 'MongoDB\\Driver\\ClientEncryption::\_\_construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::addKeyAltName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::addKeyAltName

(mongodb >=1.15.0)

MongoDB\\Driver\\ClientEncryption::addKeyAltName — Додає альтернативне ім'я до документа з ключем

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::addKeyAltName(MongoDB\BSON\Binary $keyId, string $keyAltName): ?object
```

Добавляет параметр`keyAltName` набір альтернативних імен для документа з ключем із заданим UUID `keyId`

### Список параметрів

`keyId`

Екземпляр [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md) з підтипом 4 (UUID), що ідентифікує документ із ключем.

`keyAltName`

Альтернативне ім'я для додавання документа з ключем.

### Значення, що повертаються

Повертає попередню версію документа з ключем або **`null`**, якщо жодного документа не було знайдено.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)у разі виникнення інших помилок.

### Дивіться також

-   [MongoDB\\Driver\\ClientEncryption::getKeyByAltName()](mongodb-driver-clientencryption.getkeybyaltname.md) \- Отримує документ із ключем щодо альтернативного імені
-   [MongoDB\\Driver\\ClientEncryption::removeKeyAltName()](mongodb-driver-clientencryption.removekeyaltname.md) \- Видаляє альтернативне ім'я з документа з ключем
