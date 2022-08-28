Видалити елемент із пулу опитування

-   [« ZMQPoll::poll](zmqpoll.poll.html)
    
-   [ZMQDevice »](class.zmqdevice.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQPoll](class.zmqpoll.html)
    
-   Видалити елемент із пулу опитування
    

# ZMQPoll::remove

(PECL zmq >= 0.5.0)

ZMQPoll::remove — Видалити елемент із пула опитування

### Опис

```methodsynopsis
public ZMQPoll::remove(mixed $item): bool
```

Видаляє елемент із пулу опитування. Параметр `item` повинен бути об'єктом ZMQSocket, потоковим ресурсом або ідентифікатором, отриманим у результаті виконання методу [ZMQPoll::add()](zmqpoll.add.html)

### Список параметрів

`item`

Об'єкт ZMQSocket, потік PHP або рядковий ідентифікатор елемента.

### Значення, що повертаються

Повертає **`true`**, якщо видалення виконано успішно та **`false`**, якщо елемент не знайдено.