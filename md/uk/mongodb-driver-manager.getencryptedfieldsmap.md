---
navigation:
  - mongodb-driver-manager.executewritecommand.html: '« MongoDBDriverManager::executeWriteCommand'
  - mongodb-driver-manager.getreadconcern.html: 'MongoDBDriverManager::getReadConcern »'
  - index.html: PHP Manual
  - class.mongodb-driver-manager.html: MongoDBDriverManager
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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverManager::construct()](mongodb-driver-manager.construct.html) - Створює новий Manager MongoDB
