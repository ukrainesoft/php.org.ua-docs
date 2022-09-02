---
navigation:
  - mongodb-driver-manager.executewritecommand.md: '« MongoDBDriverManager::executeWriteCommand'
  - mongodb-driver-manager.getreadconcern.md: 'MongoDBDriverManager::getReadConcern »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDBDriverManager
title: 'MongoDBDriverManager::getEncryptedFieldsMap'
---
# MongoDBDriverManager::getEncryptedFieldsMap

(mongodb >=1.14.0)

MongoDBDriverManager::getEncryptedFieldsMap — Повертає опцію автоматичного шифрування encryptedFieldsMap для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getEncryptedFieldsMap(): array|object|null
```

Повертає параметр `encryptedFieldsMap` автоматичного шифрування для Manager, якщо його вказано.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Параметр `encryptedFieldsMap` автоматичного шифрування для Manager або \*\*`null`\*\*якщо він не був вказаний.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverManager::construct()](mongodb-driver-manager.construct.md) - Створює новий Manager MongoDB
