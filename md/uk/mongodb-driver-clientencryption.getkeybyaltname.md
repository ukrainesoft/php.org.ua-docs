---
navigation:
  - mongodb-driver-clientencryption.getkey.md: '« MongoDB\\Driver\\ClientEncryption::getKey'
  - mongodb-driver-clientencryption.getkeys.md: 'MongoDB\\Driver\\ClientEncryption::getKeys »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::getKeyByAltName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::getKeyByAltName

(mongodb >=1.15.0)

MongoDB\\Driver\\ClientEncryption::getKeyByAltName — Отримує документ із ключем щодо альтернативного імені

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::getKeyByAltName(string $keyAltName): ?object
```

Знаходить єдиний документ із ключем у колекції сховища ключів із заданим альтернативним ім'ям `keyAltName`

### Список параметрів

`keyAltName`

Альтернативна назва документа з ключем.

### Значення, що повертаються

Повертає документ із ключем або **`null`**, якщо жоден документ не збігся.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)у разі виникнення інших помилок.

### Дивіться також

-   [MongoDB\\Driver\\ClientEncryption::addKeyAltName()](mongodb-driver-clientencryption.addkeyaltname.md) \- Додає альтернативне ім'я до документа із ключем
-   [MongoDB\\Driver\\ClientEncryption::removeKeyAltName()](mongodb-driver-clientencryption.removekeyaltname.md) \- Видаляє альтернативне ім'я з документа з ключем
