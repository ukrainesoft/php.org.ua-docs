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
-   [Функціональний API](functional.parallel.html)
    -   [parallelbootstrap](parallel.bootstrap.html) — Початкове завантаження
    -   [parallelrun](parallel.run.html) - Виконання
-   [parallelRuntime](class.parallel-runtime.html) - Клас parallelRuntime
    -   [parallelRuntime::construct](parallel-runtime.construct.html) - Конструктор класу Runtime
    -   [parallelRuntime::run](parallel-runtime.run.html) - Виконання
    -   [parallelRuntime::close](parallel-runtime.close.html) — Витончене з'єднання під час виконання
    -   [parallelRuntime::kill](parallel-runtime.kill.html) — З'єднання під час виконання
-   [parallelFuture](class.parallel-future.html) - Клас parallelFuture
    -   [parallelFuture::cancel](parallel-future.cancel.html) - Припинення
    -   [parallelFuture::cancelled](parallel-future.cancelled.html) — Визначення стану
    -   [parallelFuture::done](parallel-future.done.html) — Визначення стану
    -   [parallelFuture::value](parallel-future.value.html) - Розширення
-   [parallelChannel](class.parallel-channel.html) - Клас parallelChannel
    -   [parallelChannel::construct](parallel-channel.construct.html) - Конструктор класу Channel
    -   [parallelChannel::make](parallel-channel.make.html) - Доступ
    -   [parallelChannel::open](parallel-channel.open.html) - Доступ
    -   [parallelChannel::recv](parallel-channel.recv.html) - Спільне використання
    -   [parallelChannel::send](parallel-channel.send.html) - Спільне використання
    -   [parallelChannel::close](parallel-channel.close.html) - Закриття
-   [parallelEvents](class.parallel-events.html) - Клас parallelEvents
    -   [parallelEvents::setBlocking](parallel-events.setblocking.html) - Поведінка
    -   [parallelEvents::setTimeout](parallel-events.settimeout.html) - Поведінка
    -   [parallelEvents::setInput](parallel-events.setinput.html) - Вхід
    -   [parallelEvents::addChannel](parallel-events.addchannel.html) - Цілі
    -   [parallelEvents::addFuture](parallel-events.addfuture.html) - Цілі
    -   [parallelEvents::remove](parallel-events.remove.html) - Цілі
    -   [parallelEvents::poll](parallel-events.poll.html) - Опитування
-   [parallelEventsInput](class.parallel-events-input.html) - Клас parallelEventsInput
    -   [parallelEventsInput::add](parallel-events-input.add.html) - Входи
    -   [parallelEventsInput::clear](parallel-events-input.clear.html) - Входи
    -   [parallelEventsInput::remove](parallel-events-input.remove.html) - Входи
-   [parallelEventsEvent](class.parallel-events-event.html) - Клас parallelEventsEvent
-   [parallelEventsEventType](class.parallel-events-event-type.html) - Клас parallelEventsEventType
-   [parallelSync](class.parallel-sync.html) - Клас parallelSync
    -   [parallelSync::construct](parallel-sync.construct.html) - Конструктор класу
    -   [parallelSync::get](parallel-sync.get.html) - Доступ
    -   [parallelSync::set](parallel-sync.set.html) - Доступ
    -   [parallelSync::wait](parallel-sync.wait.html) - Синхронізація
    -   [parallelSync::notify](parallel-sync.notify.html) - Синхронізація
    -   [parallelSync::invoke](parallel-sync.invoke.html) - Синхронізація