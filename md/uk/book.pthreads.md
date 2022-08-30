pthreads

-   [« parallelSync::invoke](parallel-sync.invoke.html)
    
-   [Введение »](intro.pthreads.html)
    
-   [PHP Manual](index.html)
    
-   [Модули для управления процессами программ](refs.fileprocess.process.html)
    
-   pthreads
    

# pthreads

-   [Введение](intro.pthreads.html)
-   [Установка и настройка](pthreads.setup.html)
    -   [Требования](pthreads.requirements.html)
    -   [Установка](pthreads.installation.html)
    -   [Настройка во время выполнения](pthreads.configuration.html)
-   [Предопределённые константы](pthreads.constants.html)
-   [Threaded](class.threaded.html) - Клас Threaded
    -   [Threaded::chunk](threaded.chunk.html) - Обробка
    -   [Threaded::count](threaded.count.html) - Обробка
    -   [Threaded::extend](threaded.extend.html) - Обробка під час виконання
    -   [Threaded::isRunning](thread.isrunning.html) — Визначення стану
    -   [Threaded::isTerminated](threaded.isterminated.html) — Визначення стану
    -   [Threaded::merge](threaded.merge.html) - Обробка
    -   [Threaded::notify](threaded.notify.html) - Синхронізація
    -   [Threaded::notifyOne](threaded.notifyone.html) - Синхронізація
    -   [Threaded::pop](threaded.pop.html) - Обробка
    -   [Threaded::run](threaded.run.html) - Виконання
    -   [Threaded::shift](threaded.shift.html) - Обробка
    -   [Threaded::synchronized](threaded.synchronized.html) - Синхронізація
    -   [Threaded::wait](threaded.wait.html) - Синхронізація
-   [Thread](class.thread.html) - Клас Thread
    -   [Thread::getCreatorId](thread.getcreatorid.html) - Ідентифікація
    -   [Thread::getCurrentThread](thread.getcurrentthread.html) - Ідентифікація
    -   [Thread::getCurrentThreadId](thread.getcurrentthreadid.html) - Ідентифікація
    -   [Thread::getThreadId](thread.getthreadid.html) - Ідентифікація
    -   [Thread::isJoined](thread.isjoined.html) — Визначення стану
    -   [Thread::isStarted](thread.isstarted.html) — Визначення стану
    -   [Thread::join](thread.join.html) - Синхронізація
    -   [Thread::start](thread.start.html) - Виконання
-   [Worker](class.worker.html) - Клас Worker
    -   [Worker::collect](worker.collect.html) — Зібрати посилання на завершені завдання
    -   [Worker::getStacked](worker.getstacked.html) — Повертає поточний розмір стека
    -   [Worker::isShutdown](worker.isshutdown.html) — Визначення стану
    -   [Worker::shutdown](worker.shutdown.html) - Зупинити Worker
    -   [Worker::stack](worker.stack.html) — Покласти завдання на стек
    -   [Worker::unstack](worker.unstack.html) — Забрати завдання зі стека
-   [Collectable](class.collectable.html) - Інтерфейс Collectable
    -   [Collectable::isGarbage](collectable.isgarbage.html) — Визначає, чи позначений об'єкт як сміття
-   [Pool](class.pool.html) - Клас Pool
    -   [Pool::collect](pool.collect.html) — Збирає посилання на виконані завдання
    -   [Pool::construct](pool.construct.html) - Створює новий пул воркерів
    -   [Pool::resize](pool.resize.html) - Змінює розмір пулу
    -   [Pool::shutdown](pool.shutdown.html) - Вимикає всі воркери
    -   [Pool::submit](pool.submit.html) - Відправляє об'єкт на виконання
    -   [Pool::submitTo](pool.submitTo.html) — Надсилає завдання конкретному воркеру для виконання
-   [Volatile](class.volatile.html) - Клас Volatile