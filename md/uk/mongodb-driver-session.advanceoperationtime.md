Збільшує час операції для сеансу

-   [« MongoDB\\Driver\\Session::advanceClusterTime](mongodb-driver-session.advanceclustertime.html)
    
-   [MongoDB\\Driver\\Session::commitTransaction »](mongodb-driver-session.committransaction.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Збільшує час операції для сеансу
    

# MongoDBDriverSession::advanceOperationTime

(mongodb >=1.4.0)

MongoDBDriverSession::advanceOperationTime — Збільшує час операції для сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::advanceOperationTime(MongoDB\BSON\TimestampInterface $operationTime): void
```

Збільшує час операції для сеансу. Якщо час операції менше або дорівнює поточному часу сеансу, функція не працюватиме.

Використовуючи цей метод у поєднанні з [MongoDB\\Driver\\Session::advanceClusterTime()](mongodb-driver-session.advanceclustertime.html) Для копіювання операції та часу кластеризації з іншого сеансу, ви можете гарантувати, що операції у цьому сеансі причинно узгоджуються з останньою операцією на іншому сеансі.

### Список параметрів

`operationTime`

Час операції є логічною відміткою часу. Як правило, це значення буде отримано шляхом виклику [MongoDB\\Driver\\Session::getOperationTime()](mongodb-driver-session.getoperationtime.html) для іншого об'єкта сеансу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Session::advanceClusterTime()](mongodb-driver-session.advanceclustertime.html) - Збільшує час кластера для сеансу
-   [MongoDB\\Driver\\Session::getClusterTime()](mongodb-driver-session.getclustertime.html) - Повертає час кластера для цього сеансу