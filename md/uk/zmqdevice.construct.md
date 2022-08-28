Створює новий пристрій

-   [« ZMQDevice](class.zmqdevice.html)
    
-   [ZMQDevice::getIdleTimeout »](zmqdevice.getidletimeout.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQDevice](class.zmqdevice.html)
    
-   Створює новий пристрій
    

# ZMQDevice::construct

(PECL zmq >= 0.5.0)

ZMQDevice::construct — Створює новий пристрій

### Опис

```methodsynopsis
public ZMQDevice::__construct(ZMQSocket $frontend, ZMQSocket $backend, ZMQSocket $listener = ?)
```

Пристрої ØMQ можуть представляти адреси, служби, черги або будь-яку іншу абстракцію, яку потрібно визначити над шарами повідомлень і сокетів.

### Список параметрів

`frontend`

Фронтенд пристрою. Зазвичай сюди надходять повідомлення.

`backend`

Бекенд пристрою. Зазвичай звідси повідомлення надсилаються.

`listener`

Сокет слухач, який приймає копії всіх повідомлень, які приймаються або надсилаються. Тип сокету має бути SUB, PULL чи DEALER.

### Значення, що повертаються

Виклик цього методу готує пристрій. Зазвичай пристрої використовуються для довготривалих завдань, так що викликати цей метод з інтерактивних скриптів не рекомендується. У випадку, якщо пристрій не вдалося запустити, виключається виняток ZMQDeviceException.