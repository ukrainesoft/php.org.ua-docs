parallel

-   [« system](function.system.html)
    
-   [Введение »](intro.parallel.html)
    
-   [PHP Manual](index.html)
    
-   [Модули для управления процессами программ](refs.fileprocess.process.html)
    
-   parallel
    

# parallel

-   [Введение](intro.parallel.html)
-   [Установка](parallel.setup.html)
-   [Философия](philosophy.parallel.html)
-   [Функциональный API](functional.parallel.html)
    -   [parallel\\bootstrap](parallel.bootstrap.html) — Початкове завантаження
    -   [parallel\\run](parallel.run.html) - Виконання
-   [parallel\\Runtime](class.parallel-runtime.html) - Клас parallelRuntime
    -   [parallel\\Runtime::\_\_construct](parallel-runtime.construct.html) - Конструктор класу Runtime
    -   [parallel\\Runtime::run](parallel-runtime.run.html) - Виконання
    -   [parallel\\Runtime::close](parallel-runtime.close.html) — Витончене з'єднання під час виконання
    -   [parallel\\Runtime::kill](parallel-runtime.kill.html) — З'єднання під час виконання
-   [parallel\\Future](class.parallel-future.html) - Клас parallelFuture
    -   [parallel\\Future::cancel](parallel-future.cancel.html) - Припинення
    -   [parallel\\Future::cancelled](parallel-future.cancelled.html) — Визначення стану
    -   [parallel\\Future::done](parallel-future.done.html) — Визначення стану
    -   [parallel\\Future::value](parallel-future.value.html) - Розширення
-   [parallel\\Channel](class.parallel-channel.html) - Клас parallelChannel
    -   [parallel\\Channel::\_\_construct](parallel-channel.construct.html) - Конструктор класу Channel
    -   [parallel\\Channel::make](parallel-channel.make.html) - Доступ
    -   [parallel\\Channel::open](parallel-channel.open.html) - Доступ
    -   [parallel\\Channel::recv](parallel-channel.recv.html) - Спільне використання
    -   [parallel\\Channel::send](parallel-channel.send.html) - Спільне використання
    -   [parallel\\Channel::close](parallel-channel.close.html) - Закриття
-   [parallel\\Events](class.parallel-events.html) - Клас parallelEvents
    -   [parallel\\Events::setBlocking](parallel-events.setblocking.html) - Поведінка
    -   [parallel\\Events::setTimeout](parallel-events.settimeout.html) - Поведінка
    -   [parallel\\Events::setInput](parallel-events.setinput.html) - Вхід
    -   [parallel\\Events::addChannel](parallel-events.addchannel.html) - Цілі
    -   [parallel\\Events::addFuture](parallel-events.addfuture.html) - Цілі
    -   [parallel\\Events::remove](parallel-events.remove.html) - Цілі
    -   [parallel\\Events::poll](parallel-events.poll.html) - Опитування
-   [parallel\\Events\\Input](class.parallel-events-input.html) - Клас parallelEventsInput
    -   [parallel\\Events\\Input::add](parallel-events-input.add.html) - Входи
    -   [parallel\\Events\\Input::clear](parallel-events-input.clear.html) - Входи
    -   [parallel\\Events\\Input::remove](parallel-events-input.remove.html) - Входи
-   [parallel\\Events\\Event](class.parallel-events-event.html) - Клас parallelEventsEvent
-   [parallel\\Events\\Event\\Type](class.parallel-events-event-type.html) - Клас parallelEventsEventType
-   [parallel\\Sync](class.parallel-sync.html) - Клас parallelSync
    -   [parallel\\Sync::\_\_construct](parallel-sync.construct.html) - Конструктор класу
    -   [parallel\\Sync::get](parallel-sync.get.html) - Доступ
    -   [parallel\\Sync::set](parallel-sync.set.html) - Доступ
    -   [parallel\\Sync::wait](parallel-sync.wait.html) - Синхронізація
    -   [parallel\\Sync::notify](parallel-sync.notify.html) - Синхронізація
    -   [parallel\\Sync::\_\_invoke](parallel-sync.invoke.html) - Синхронізація