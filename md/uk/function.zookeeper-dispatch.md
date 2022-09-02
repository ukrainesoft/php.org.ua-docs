---
navigation:
  - ref.zookeeper.md: « Функции ZooKeeper
  - class.zookeeper.md: Zookeeper »
  - index.md: PHP Manual
  - ref.zookeeper.md: Функции ZooKeeper
title: zookeeperdispatch
---
# zookeeperdispatch

(PECL zookeeper >= 0.4.0)

zookeeperdispatch — Викликати callback-функції для операцій, що очікують.

### Опис

```methodsynopsis
zookeeper_dispatch(): void
```

Функція **zookeeperdispatch()** викликає callback-функції, передані операціями, такими як [Zookeeper::get()](zookeeper.get.md) або [Zookeeper::exists()](zookeeper.exists.md)

**Застереження**

З версії 0.4.0 ця функція має бути викликана вручну для асинхронних операцій. Якщо ви хочете, щоб це було зроблено автоматично, ви можете оголосити тики на початку скрипту, використовуючи директиву declare.

Після PHP 7.1 можна ігнорувати цю функцію. Модуль використовує EG (vminterrupt) для реалізації асинхронного виклику callback-функцій.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Ця функція викликає попередження PHP, якщо callback-функція не може бути викликана.

### Приклади

**Приклад #1 **zookeeperdispatch()** example #1**

Виклик callback-функцій вручну.

```php
<?php
$client = new Zookeeper();
$client->connect('localhost:2181');
$client->get('/zookeeper', function() {
    echo "Была вызвана callback-функция".PHP_EOL;
});
while(true) {
    sleep(1);
    zookeeper_dispatch();
}
?>
```

**Приклад #2 Приклад використання **zookeeperdispatch()****

Оголошення тиків.

```php
<?php
declare(ticks=1);

$client = new Zookeeper();
$client->connect('localhost:2181');
$client->get('/zookeeper', function() {
    echo "Была вызвана callback-функция".PHP_EOL;
});
while(true) {
    sleep(1);
}
?>
```

### Дивіться також

-   [Zookeeper::addAuth()](zookeeper.addauth.md) - Вказує облікові дані програми
-   [Zookeeper::connect()](zookeeper.connect.md) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::construct()](zookeeper.construct.md) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::exists()](zookeeper.exists.md) - Синхронно перевіряє наявність вузла в zookeeper
-   [Zookeeper::get()](zookeeper.get.md) - Синхронно отримує дані, пов'язані з вузлом
-   [Zookeeper::getChildren()](zookeeper.getchildren.md) - Виводить список нащадків вузла синхронно
-   [Zookeeper::setWatcher()](zookeeper.setwatcher.md) - Встановлює функцію спостерігача
