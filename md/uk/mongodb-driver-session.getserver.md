---
navigation:
  - mongodb-driver-session.getoperationtime.md: '« MongoDB\\Driver\\Session::getOperationTime'
  - mongodb-driver-session.gettransactionoptions.md: 'MongoDB\\Driver\\Session::getTransactionOptions »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::getServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::getServer

(mongodb >=1.6.0)

MongoDB\\Driver\\Session::getServer — Повертає сервер, до якого прив'язана поточна сесія.

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getServer(): ?MongoDB\Driver\Server
```

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md)до якого прив'язана поточна сесія. Якщо сесія не прив'язана до сервера, то буде повернено **`null`**

Прив'язка сесії в основному використовується для шардованих транзакцій, тому що всі команди повинні йти на той самий екземпляр mongos. Цей метод призначений для використання в бібліотеках, побудованих поверх модуля, щоб можна було закріпити сервер, а не вибирати сервер кожної наступної команди.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md)к которому прикреплена сессия. Или\*\*`null`\*\*, якщо сесія не прикріплена до жодного сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
