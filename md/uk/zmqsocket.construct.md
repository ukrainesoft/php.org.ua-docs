Конструктор класу ZMQSocket

-   [« ZMQSocket::connect](zmqsocket.connect.html)
    
-   [ZMQSocket::disconnect »](zmqsocket.disconnect.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQSocket](class.zmqsocket.html)
    
-   Конструктор класу ZMQSocket
    

# ZMQSocket::construct

(PECL zmq >= 0.5.0)

ZMQSocket::construct - Конструктор класу ZMQSocket

### Опис

```methodsynopsis
public ZMQSocket::__construct(    ZMQContext $context,    int $type,    string $persistent_id = null,    callable $on_new_socket = null)
```

Створює екземпляр класу ZMQSocket. Параметр `persistent_id` може бути використаний для встановлення постійного з'єднання. Постійний сокет буде виділено з постійного контексту і залишатиметься активним протягом кількох запитів. Отримати той самий сокет для багатьох запитів можна за допомогою параметра `persistent_id`. Функція, задана в `on_new_socket` викликається лише за створенні нової структури сокету.

### Список параметрів

`context`

Об'єкт класу ZMQContext.

`type`

Тип сокету. Дивіться константи **`ZMQ::SOCKET_*`**

`persistent_id`

Якщо параметр `persistent_id` вказано, що сокет буде доступний протягом декількох запитів. Якщо `context` не є постійним, сокет також повернеться до непостійного режиму.

`on_new_socket`

Callback-функція, яка буде викликана під час створення нового сокету. Ця функція не викликається у разі повторного використання постійного з'єднання.

```methodsynopsis
callback(ZMQSocket $socket, string $persistent_id = null)
```

### Помилки

Викидає **ZMQSocketException** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ZMQSocket()****

Використання функції зворотного дзвінка для зв'язку або підключення до сокету

```php
<?php

/*
  Здесь используется постоянный сокет, поэтому функция будет вызвана лишь
  при первом обращении к скрипту.
*/
function on_new_socket_cb(ZMQSocket $socket, $persistent_id = null)
{
    if ($persistent_id === 'server') {
        $socket->bind("tcp://localhost:12122");
    } else {
        $socket->connect("tcp://localhost:12122");
    }
}

/* Создать новый контекст */
$context = new ZMQContext();

/* Создать сокет */
$socket = $context->getSocket(ZMQ::SOCKET_REP, 'server', 'on_new_socket_cb');

$message = $socket->recv();
echo "Получено сообщение: {$message}\n";
?>
```