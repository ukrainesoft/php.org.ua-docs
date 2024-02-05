---
navigation:
  - zmqpoll.getlasterrors.md: '« ZMQPoll::getLastErrors'
  - zmqpoll.remove.md: 'ZMQPoll::remove »'
  - index.md: PHP Manual
  - class.zmqpoll.md: ZMQPoll
title: 'ZMQPoll::poll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQPoll::poll

(PECL zmq >= 0.5.0)

ZMQPoll::poll — Опитати всі елементи пулу

### Опис

```methodsynopsis
public ZMQPoll::poll(array &$readable, array &$writable, int $timeout = -1): int
```

Опитує всі елементи пулу. Читані та записувані елементи містяться у параметрах `readable`и`writable` відповідно. Для перевірки помилок використовуйте метод [ZMQPoll::getLastErrors()](zmqpoll.getlasterrors.md)

### Список параметрів

`readable`

Масив, в який будуть повернуті об'єкти, що читаються ZMQSockets/потоки PHP. Перед початком роботи масив буде очищений.

`writable`

Масив, в який будуть повернуті записані об'єкти ZMQSockets/потоки PHP. Перед початком роботи масив буде очищений.

`timeout`

Час очікування операції. -1 означає, що опитування чекатиме до останнього. Зверніть увагу, що з версії 1.0.0 час очікування задається в мілісекундах, а не в мікросекундах, як раніше.

### Значення, що повертаються

Повертає кількість елементів, котрим відбувалася якась активність.

### Помилки

Викидає **ZMQPollException**в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** ZMQPoll()\*\*\*\*

Створимо простий сервер опитування

```php
<?php

/* Создаём сокет, паттерн request-reply (отвечающий сокет) */
$context = new ZMQContext();
$server  = $context->getSocket(ZMQ::SOCKET_REP);

/* Привязываем к порту 5555 на адрес 127.0.0.1 */
$server->bind("tcp://127.0.0.1:5555");

/* Создаём новый пул опроса для входящих/исходящих сообщений */
$poll = new ZMQPoll();

/* Добавляем объект и слушаем на предмет опроса входящих/исходящих */
$id = $poll->add($server, ZMQ::POLL_IN | ZMQ::POLL_OUT);
echo "Added object with id " . $id . "\n";

/* Инициализируем массив читаемых и записываемых элементов */
$readable = array();
$writable = array();

while (true) {
   /* Количество извлечённых событий */
   $events = 0;

   try {
       /* Опрашиваем, пока есть что делать */
       $events = $poll->poll($readable, $writable, -1);
       $errors = $poll->getLastErrors();

       if (count($errors) > 0) {
           foreach ($errors as $error) {
               echo "Ошибка опроса объекта " . $error . "\n";
           }
       }
   } catch (ZMQPollException $e) {
       echo "Опрос не удался: " . $e->getMessage() . "\n";
   }

   if ($events > 0) {
       /* Перебираем читаемые объекты и получаем сообщения */
       foreach ($readable as $r) {
           try {
               echo "Получено сообщение: " . $r->recv() . "\n";
           } catch (ZMQException $e) {
               echo "Ошибка получения: " . $e->getMessage() . "\n";
           }
       }

       /* Перебираем записываемые объекты и отправляем ответы */
       foreach ($writable as $w) {
           try {
               $w->send("Получил!");
           } catch (ZMQException $e) {
               echo "Ошибка отправки: " . $e->getMessage() . "\n";
           }
       }
   }
}
?>
```
