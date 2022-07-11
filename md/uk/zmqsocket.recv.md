- [« ZMQSocket::isPersistent](zmqsocket.ispersistent.md)
- [ZMQSocket::recvMulti »](zmqsocket.recvmulti.md)

- [PHP Manual](index.md)
- [ZMQSocket](class.zmqsocket.md)
-   Отримати повідомлення

# ZMQSocket::recv

(PECL zmq \>= 0.5.0)

ZMQSocket::recv — Отримати повідомлення

### Опис

public **ZMQSocket::recv**(int `$mode` = 0): string

Отримує повідомлення із сокету. За замовчуванням отримання блокуватиметься
до того часу, поки повідомлення не буде доступне, тільки якщо не встановлено
прапор **`ZMQ::MODE_DONTWAIT`**. Можна використовувати опцію сокету
**`ZMQ::SOCKOPT_RCVMORE`** для отримання повідомлень, що складаються з
кількох частин. Детальніше дивіться
[ZMQSocket::setSockOpt()](zmqsocket.setsockopt.md).

### Список параметрів

`mode`
Прапори для налаштування режиму не блокуючого отримання та роботи з
повідомленнями, що з кількох частин. Дивіться константи
**`ZMQ::MODE_*`**.

### Значення, що повертаються

Повертає повідомлення. Якщо використовується режим **`ZMQ::MODE_DONTWAIT`** та
операцію заблоковано, то буде повернено **`false`**.

### Помилки

Викидає **ZMQSocketException** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад відправлення/одержання**

Не блокуюча відправка/отримання

`<?php/* Створюємо новий об'єкт черги. Необхідний сервер на іншій стороні. */$queue = new ZMQSocket(new ZMQContext(), ZMQ::SOCKET_REQ);$queue->connect("tcp://127.0.0.1:5555");/* Прив'язуємо сокет 1 к /$retries = 5;$sending = true;/* Запускаем цикл */do {    try {        /* Пытаемся отправить/получить */        if ($sending) {            echo "Отправляем сообщение
";            $queue->send("Я сообщение!", ZMQ::MODE_DONTWAIT);            $sending = false;        } else {            echo "Получен ответ: " . $queue->recv(ZMQ::MODE_DONTWAIT) . "
";            break;        }    } catch (ZMQSocketException $e) {        /* EAGAIN означает, что операция заблокирована, повторяем */        if ($e->getCode() === ZMQ::ERR_EAGAIN) {            echo " - Получили EAGAIN, повторяем ($retries)
";        } else {            die(" - Ошибка: " . $e->getMessage());        }    }    /* Немножко ждём */    usleep(5);} while (--$retries);?> `

Результатом виконання цього прикладу буде щось подібне:

Надсилаємо повідомлення
- Отримали EAGAIN, повторюємо (4)
Отримано відповідь: Я повідомлення!
