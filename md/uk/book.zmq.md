ZMQ

-   [« yaz\_wait](function.yaz-wait.html)
    
-   [Введение »](intro.zmq.html)
    
-   [PHP Manual](index.html)
    
-   [Другие службы](refs.remote.other.html)
    
-   ZMQ
    

# ZMQ

-   [Введение](intro.zmq.html)
-   [Установка и настройка](zmq.setup.html)
    -   [Требования](zmq.requirements.html)
-   [ZMQ](class.zmq.html) - Клас ZMQ
    -   [ZMQ::\_\_construct](zmq.construct.html) - Конструктор ZMQ
-   [ZMQContext](class.zmqcontext.html) - Клас ZMQContext
    -   [ZMQContext::\_\_construct](zmqcontext.construct.html) - Конструктор ZMQContext
    -   [ZMQContext::getOpt](zmqcontext.getopt.html) — Отримати опцію контексту
    -   [ZMQContext::getSocket](zmqcontext.getsocket.html) - Створює новий сокет
    -   [ZMQContext::isPersistent](zmqcontext.ispersistent.html) — Чи контекст є постійним
    -   [ZMQContext::setOpt](zmqcontext.setopt.html) - Встановити опцію сокету
-   [ZMQSocket](class.zmqsocket.html) - Клас ZMQSocket
    -   [ZMQSocket::bind](zmqsocket.bind.html) - Прив'язка сокету
    -   [ZMQSocket::connect](zmqsocket.connect.html) — Підключення до сокету
    -   [ZMQSocket::\_\_construct](zmqsocket.construct.html) - Конструктор класу ZMQSocket
    -   [ZMQSocket::disconnect](zmqsocket.disconnect.html) - Вимкнути сокет
    -   [ZMQSocket::getEndpoints](zmqsocket.getendpoints.html) — Отримати список кінцевих точок
    -   [ZMQSocket::getPersistentId](zmqsocket.getpersistentid.html) - Отримати ідентифікатор постійного сокету
    -   [ZMQSocket::getSocketType](zmqsocket.getsockettype.html) — Отримати тип сокету
    -   [ZMQSocket::getSockOpt](zmqsocket.getsockopt.html) - Отримати опцію сокету
    -   [ZMQSocket::isPersistent](zmqsocket.ispersistent.html) — Визначити, чи є сокет постійним
    -   [ZMQSocket::recv](zmqsocket.recv.html) - Отримати повідомлення
    -   [ZMQSocket::recvMulti](zmqsocket.recvmulti.html) — Отримати повідомлення, яке складається з кількох частин
    -   [ZMQSocket::send](zmqsocket.send.html) — Надіслати повідомлення
    -   [ZMQSocket::sendmulti](zmqsocket.sendmulti.html) — Надіслати повідомлення, яке складається з кількох частин
    -   [ZMQSocket::setSockOpt](zmqsocket.setsockopt.html) - Встановити опцію сокету
    -   [ZMQSocket::unbind](zmqsocket.unbind.html) - Відв'язати сокет
-   [ZMQPoll](class.zmqpoll.html) - Клас ZMQPoll
    -   [ZMQPoll::add](zmqpoll.add.html) — Додати елемент у пул опитування
    -   [ZMQPoll::clear](zmqpoll.clear.html) - Очистити пул опитування
    -   [ZMQPoll::count](zmqpoll.count.html) — Кількість елементів у пулі опитування
    -   [ZMQPoll::getLastErrors](zmqpoll.getlasterrors.html) — Повертає помилки останнього опитування
    -   [ZMQPoll::poll](zmqpoll.poll.html) — Опитати всі елементи пулу
    -   [ZMQPoll::remove](zmqpoll.remove.html) — Видалити елемент із пула опитування
-   [ZMQDevice](class.zmqdevice.html) - Клас ZMQDevice
    -   [ZMQDevice::\_\_construct](zmqdevice.construct.html) — Створює новий пристрій
    -   [ZMQDevice::getIdleTimeout](zmqdevice.getidletimeout.html) — Отримати час очікування бездіяльності
    -   [ZMQDevice::getTimerTimeout](zmqdevice.gettimertimeout.html) - Отримати час очікування таймера
    -   [ZMQDevice::run](zmqdevice.run.html) — Запуск нового пристрою
    -   [ZMQDevice::setIdleCallback](zmqdevice.setidlecallback.html) - Встановити callback-функцію бездіяльності
    -   [ZMQDevice::setIdleTimeout](zmqdevice.setidletimeout.html) — Встановити час очікування простою
    -   [ZMQDevice::setTimerCallback](zmqdevice.settimercallback.html) - Встановити callback-функцію за таймером
    -   [ZMQDevice::setTimerTimeout](zmqdevice.settimertimeout.html) - Встановити час очікування таймера