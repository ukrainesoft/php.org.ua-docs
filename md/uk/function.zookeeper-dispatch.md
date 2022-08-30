Викликати callback-функції для операцій, що очікують

-   [« Функции ZooKeeper](ref.zookeeper.html)
    
-   [Zookeeper »](class.zookeeper.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ZooKeeper](ref.zookeeper.html)
    
-   Викликати callback-функції для операцій, що очікують
    

# zookeeperdispatch

(PECL zookeeper >= 0.4.0)

zookeeperdispatch — Викликати callback-функції для операцій, що очікують.

### Опис

```methodsynopsis
zookeeper_dispatch(): void
```

Функція **zookeeperdispatch()** викликає callback-функції, передані операціями, такими як [Zookeeper::get()](zookeeper.get.html) або [Zookeeper::exists()](zookeeper.exists.html)

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

-   [Zookeeper::addAuth()](zookeeper.addauth.html) - Вказує облікові дані програми
-   [Zookeeper::connect()](zookeeper.connect.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::construct()](zookeeper.construct.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::exists()](zookeeper.exists.html) - Синхронно перевіряє наявність вузла в zookeeper
-   [Zookeeper::get()](zookeeper.get.html) - Синхронно отримує дані, пов'язані з вузлом
-   [Zookeeper::getChildren()](zookeeper.getchildren.html) - Виводить список нащадків вузла синхронно
-   [Zookeeper::setWatcher()](zookeeper.setwatcher.html) - Встановлює функцію спостерігача