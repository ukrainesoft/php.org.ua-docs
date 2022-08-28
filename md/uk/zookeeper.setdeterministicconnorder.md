Включення/відключення рандомізації порядку кінцевих точок кворуму

-   [« Zookeeper::setDebugLevel](zookeeper.setdebuglevel.html)
    
-   [Zookeeper::setLogStream »](zookeeper.setlogstream.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Включення/відключення рандомізації порядку кінцевих точок кворуму
    

# Zookeeper::setDeterministicConnOrder

(PECL zookeeper >= 0.1.0)

Zookeeper::setDeterministicConnOrder — Увімкнення/вимкнення рандомізації порядку кінцевих точок кворуму

### Опис

```methodsynopsis
public
   static
   Zookeeper::setDeterministicConnOrder(bool $yesOrNo): bool
```

Якщо передано значення true, клієнт підключатиметься до однорангових вузлів кворуму в порядку, вказаному у виклику zookeeperinit(). Значення false змушує zookeeperinit() переставляти однорангові кінцеві точки, що добре для рівномірного розподілу клієнтських з'єднань між одноранговими вузлами кворуму. За замовчуванням клієнт C ZooKeeper використовує false.

### Список параметрів

`yesOrNo`

Вимкнути/включити рандомізацію порядку кінцевих точок кворуму.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або типи неправильні або операція не виконується.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Дивіться також

-   [Zookeeper::\_\_construct()](zookeeper.construct.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.html) - Створює дескриптор для спілкування з zookeeper
-   [ZookeeperException](class.zookeeperexception.html)