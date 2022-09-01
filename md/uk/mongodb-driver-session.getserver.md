---
navigation:
  - mongodb-driver-session.getoperationtime.html: '« MongoDBDriverSession::getOperationTime'
  - mongodb-driver-session.gettransactionoptions.html: 'MongoDBDriverSession::getTransactionOptions »'
  - index.html: PHP Manual
  - class.mongodb-driver-session.html: MongoDBDriverSession
title: 'MongoDBDriverSession::getServer'
---
# MongoDBDriverSession::getServer

(mongodb >=1.6.0)

MongoDBDriverSession::getServer — Повертає сервер, до якого прив'язана поточна сесія.

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getServer(): ?MongoDB\Driver\Server
```

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html)до якого прив'язана поточна сесія. Якщо сесія не прив'язана до сервера, то буде повернено **`null`**

Прив'язка сесії в основному використовується для шардованих транзакцій, тому що всі команди повинні йти на той самий екземпляр mongos. Цей метод призначений для використання в бібліотеках, побудованих поверх модуля, щоб можна було закріпити сервер, а не вибирати сервер кожної наступної команди.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html) до якого прикріплено сесію. Або **`null`**, якщо сесія не прикріплена до жодного сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
