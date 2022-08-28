Збільшує час кластера для сеансу

-   [« MongoDB\\Driver\\Session::abortTransaction](mongodb-driver-session.aborttransaction.html)
    
-   [MongoDB\\Driver\\Session::advanceOperationTime »](mongodb-driver-session.advanceoperationtime.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Збільшує час кластера для сеансу
    

# MongoDBDriverSession::advanceClusterTime

(mongodb >=1.4.0)

MongoDBDriverSession::advanceClusterTime — Збільшує час кластера для сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::advanceClusterTime(array|object $clusterTime): void
```

Підвищує час кластера для сеансу. Якщо час кластера менше або дорівнює поточному часу кластера сеансу, функція не працюватиме.

Використовуючи цей метод у поєднанні з [MongoDB\\Driver\\Session::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.html) Для копіювання кластера та часу операцій з іншого сеансу, ви можете переконатися, що операції на цьому сеансі причинно відповідають останній операції в іншому сеансі.

### Список параметрів

`clusterTime`

Час кластера - це документ, що містить логічну мітку часу та сигнатуру сервера. Як правило, це значення буде отримано шляхом виклику [MongoDB\\Driver\\Session::getClusterTime()](mongodb-driver-session.getclustertime.html) для іншого об'єкта сеансу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Session::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.html) - Збільшує час операції для сеансу
-   [MongoDB\\Driver\\Session::getClusterTime()](mongodb-driver-session.getclustertime.html) - Повертає час кластера для цього сеансу