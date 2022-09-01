---
navigation:
  - mongodb-driver-session.advanceclustertime.html: '« MongoDBDriverSession::advanceClusterTime'
  - mongodb-driver-session.committransaction.html: 'MongoDBDriverSession::commitTransaction »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.html: MongoDBDriverSession
title: 'MongoDBDriverSession::advanceOperationTime'
---
# MongoDBDriverSession::advanceOperationTime

(mongodb >=1.4.0)

MongoDBDriverSession::advanceOperationTime — Збільшує час операції для сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::advanceOperationTime(MongoDB\BSON\TimestampInterface $operationTime): void
```

Збільшує час операції для сеансу. Якщо час операції менше або дорівнює поточному часу сеансу, функція не працюватиме.

Використовуючи цей метод у поєднанні з [MongoDBDriverSession::advanceClusterTime()](mongodb-driver-session.advanceclustertime.html) Для копіювання операції та часу кластеризації з іншого сеансу, ви можете гарантувати, що операції у цьому сеансі причинно узгоджуються з останньою операцією на іншому сеансі.

### Список параметрів

`operationTime`

Час операції є логічною відміткою часу. Як правило, це значення буде отримано шляхом виклику [MongoDBDriverSession::getOperationTime()](mongodb-driver-session.getoperationtime.html) для іншого об'єкта сеансу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverSession::advanceClusterTime()](mongodb-driver-session.advanceclustertime.html) - Збільшує час кластера для сеансу
-   [MongoDBDriverSession::getClusterTime()](mongodb-driver-session.getclustertime.html) - Повертає час кластера для цього сеансу
