---
navigation:
  - zookeeper.setdebuglevel.md: '« Zookeeper::setDebugLevel'
  - zookeeper.setlogstream.md: 'Zookeeper::setLogStream »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::setDeterministicConnOrder'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::setDeterministicConnOrder

(PECL zookeeper >= 0.1.0)

Zookeeper::setDeterministicConnOrder — Увімкнення/вимкнення рандомізації порядку кінцевих точок кворуму

### Опис

```methodsynopsis
public
   static
   Zookeeper::setDeterministicConnOrder(bool $yesOrNo): bool
```

Якщо передано значення true, клієнт підключатиметься до однорангових вузлів кворуму в порядку, вказаному у виклику zookeeper\_init(). Значення false змушує zookeeper\_init() переставляти однорангові кінцеві точки, що добре для рівномірного розподілу клієнтських з'єднань між одноранговими вузлами кворуму. За замовчуванням клієнт C ZooKeeper використовує false.

### Список параметрів

`yesOrNo`

Вимкнути/включити рандомізацію порядку кінцевих точок кворуму.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або типи неправильні або операція не виконується.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Дивіться також

-   [Zookeeper::\_\_construct()](zookeeper.construct.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.md) \- Створює дескриптор для спілкування з zookeeper
-   [ZookeeperException](class.zookeeperexception.md)
