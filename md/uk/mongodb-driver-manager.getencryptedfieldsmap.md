---
navigation:
  - mongodb-driver-manager.executewritecommand.md: '« MongoDB\\Driver\\Manager::executeWriteCommand'
  - mongodb-driver-manager.getreadconcern.md: 'MongoDB\\Driver\\Manager::getReadConcern »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::getEncryptedFieldsMap'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::getEncryptedFieldsMap

(mongodb >=1.14.0)

MongoDB\\Driver\\Manager::getEncryptedFieldsMap — Повертає опцію автоматичного шифрування encryptedFieldsMap для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getEncryptedFieldsMap(): array|object|null
```

Возвращает параметр`encryptedFieldsMap` автоматичного шифрування для Manager, якщо його вказано.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Параметр`encryptedFieldsMap` автоматичного шифрування для Manager або \*\*`null`\*\*якщо він не був вказаний.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Manager::\_\_construct()](mongodb-driver-manager.construct.md) \- Створює новий Manager MongoDB
