---
navigation:
  - ev.periodic-modes.md: « Режими роботи періодичних спостерігачів
  - ev.backend.md: 'Ev::backend »'
  - index.md: PHP Manual
  - book.ev.md: Єв
title: Клас Ev
---
# Клас Ev

(PECL ev >= 0.2.0)

## Вступ

Клас EV є статичним класом, забезпечуючи доступ до циклу за замовчуванням та деяким поширеним операціям.

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class Ev
     
     {
    
    /* Константы */
    
    
     const
     int
      FLAG_AUTO = 0;

    const
     int
      FLAG_NOENV = 16777216;

    const
     int
      FLAG_FORKCHECK = 33554432;

    const
     int
      FLAG_NOINOTIFY = 1048576;

    const
     int
      FLAG_SIGNALFD = 2097152;

    const
     int
      FLAG_NOSIGMASK = 4194304;

    const
     int
      RUN_NOWAIT = 1;

    const
     int
      RUN_ONCE = 2;

    const
     int
      BREAK_CANCEL = 0;

    const
     int
      BREAK_ONE = 1;

    const
     int
      BREAK_ALL = 2;

    const
     int
      MINPRI = -2;

    const
     int
      MAXPRI = 2;

    const
     int
      READ = 1;

    const
     int
      WRITE = 2;

    const
     int
      TIMER = 256;

    const
     int
      PERIODIC = 512;

    const
     int
      SIGNAL = 1024;

    const
     int
      CHILD = 2048;

    const
     int
      STAT = 4096;

    const
     int
      IDLE = 8192;

    const
     int
      PREPARE = 16384;

    const
     int
      CHECK = 32768;

    const
     int
      EMBED = 65536;

    const
     int
      CUSTOM = 16777216;

    const
     int
      ERROR = 2147483648;

    const
     int
      BACKEND_SELECT = 1;

    const
     int
      BACKEND_POLL = 2;

    const
     int
      BACKEND_EPOLL = 4;

    const
     int
      BACKEND_KQUEUE = 8;

    const
     int
      BACKEND_DEVPOLL = 16;

    const
     int
      BACKEND_PORT = 32;

    const
     int
      BACKEND_ALL = 63;

    const
     int
      BACKEND_MASK = 65535;

    
    /* Методы */
    
   final
   public
   static
   backend(): int
final
   public
   static
   depth(): int
final
   public
   static
   embeddableBackends(): int
final
   public
   static
   feedSignal(
    int
     $signum
   ): void
final
   public
   static
   feedSignalEvent(
    int
     $signum
   ): void
final
   public
   static
   iteration(): int
final
   public
   static
   now(): float
final
   public
   static
   nowUpdate(): void
final
   public
   static
   recommendedBackends(): int
final
   public
   static
   resume(): void
final
   public
   static
   run(
    int
     $flags
    = ?): void
final
   public
   static
   sleep(
    float
     $seconds
   ): void
final
   public
   static
   stop(
    int
     $how
    = ?): void
final
   public
   static
   supportedBackends(): int
final
   public
   static
   suspend(): void
final
   public
   static
   time(): float
final
   public
   static
   verify(): void

   }
```

## Обумовлені константи

Прапори, що передаються під час створення циклу:

**`Ev::FLAG_AUTO`**

Задає прапори значення за замовчуванням

**`Ev::FLAG_NOENV`**

Якщо прапор використовується (або програма запускає setuid або setgid), то `libev` не дивиться на змінну оточення LIBEVFLAGS. В іншому випадку (за умовчанням), якщо знайдено LIBEVFLAGS, то він повністю перевизначає прапори. Корисно для тестів продуктивності та пошуку помилок.

**`Ev::FLAG_FORKCHECK`**

Примушує libev перевіряти розгалуження в кожній ітерації замість виклику [EvLoop::fork()](evloop.fork.md) вручну. Це працює шляхом виклику `getpid()` на кожній ітерації циклу, і, таким чином, це може уповільнити роботу циклу подій з великою кількістю циклів ітерацій, але зазвичай не сильно. Цей прапор не може бути перевизначений або вказаний у змінному середовищі LIBEVFLAGS.

**`Ev::FLAG_NOINOTIFY`**

Якщо цей прапор вказано, то `libev` не намагатиметься використовувати API `inotify` для своїх спостерігачів [» evstat](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_stat_code_did_the_file_attri) Прапор може бути корисним для збереження файлових дескрипторів inotify, інакше кожен цикл, що використовує спостерігачів `ev_stat`, споживатиме один дескриптор `inotify`

**`Ev::FLAG_SIGNALFD`**

Якщо прапор вказано, то `libev` намагатиметься використовувати API `signalfd` для своїх спостерігачів [» evsignal](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_signal_code_signal_me_when_a) (і [» evchild](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_child_code_watch_out_for_pro)). API передає сигнали синхронно, що робить його швидшим і, можливо, дозволить отримати дані з черги сигналів, а також дозволяє спростити обробку сигналів за допомогою потоків, оскільки сигнали коректно блокуються в потоках . `Signalfd` не використовується за замовчуванням.

**`Ev::FLAG_NOSIGMASK`**

Якщо вказано прапор, то `libev` уникатиме зміни маски сигналу. Зокрема це застосовується, щоб перед отриманням сигналу переконатися, що він розблокований.

Така поведінка корисна для обробки сигналів користувача або обробки сигналів тільки певних потоків.

Прапори, що передаються в [Ev::run()](ev.run.md), або [EvLoop::run()](evloop.run.md)

**`Ev::RUN_NOWAIT`**

Означає, що цикл подій шукатиме і оброблятиме нові події, а також будь-які очікувані виконання події з них, але не чекатиме і блокуватиме процес у разі, якщо не було жодних подій і завершиться після однієї ітерації циклу. Це іноді корисно для опитування та опрацювання нових подій під час виконання тривалих обчислень, зберігаючи при цьому можливість взаємодії з програмою.

**`Ev::RUN_ONCE`**

Означає, що цикл подій шукатиме нові події (очікуючи, у разі потреби) та обробляти ці та будь-які вже очікуючі події з них. Він блокуватиме процес, доки не надійде принаймні одна нова подія (це може бути внутрішня подія libev, тому немає жодної гарантії, що буде викликана задана callback-функція) і завершиться після однієї ітерації циклу.

Прапори, що передаються в [Ev::stop()](ev.stop.md) , або [EvLoop::stop()](evloop.stop.md)

**`Ev::BREAK_CANCEL`**

Скасування операції переривання.

**`Ev::BREAK_ONE`**

Повертає найглибший запит [Ev::run()](ev.run.md) (або [EvLoop::run()](evloop.run.md)

**`Ev::BREAK_ALL`**

Завершує всі вкладені дзвінки [Ev::run()](ev.run.md) (або [EvLoop::run()](evloop.run.md)

Пріоритети спостерігачів:

**`Ev::MINPRI`**

Мінімально допустимий пріоритет спостерігача.

**`Ev::MAXPRI`**

Найбільш допустимий пріоритет спостерігача.

Побутові маски (отриманих) подій:

**`Ev::READ`**

Дескриптор файлу у спостерігачі [EvIo](class.evio.md) доступний для читання.

**`Ev::WRITE`**

Дескриптор файлу у спостерігачі [EvIo](class.evio.md) доступний для запису.

**`Ev::TIMER`**

[EvTimer](class.evtimer.md) спостерігає за перевищенням ліміту часу.

**`Ev::PERIODIC`**

[EvPeriodic](class.evperiodic.md) спостерігає за перевищенням ліміту часу.

**`Ev::SIGNAL`**

Вказаний у [EvSignal::construct()](evsignal.construct.md) сигнал отримано.

**`Ev::CHILD`**

`pid` Вказаний у [EvChild::construct()](evchild.construct.md) отримано і статус змінено.

**`Ev::STAT`**

Шлях, вказаний у спостерігачі [EvStat](class.evstat.md) змінив свої атрибути.

**`Ev::IDLE`**

Спостерігач [EvIdle](class.evidle.md) працює, коли решта спостерігачів нічого не робить.

**`Ev::PREPARE`**

Усі спостерігачі [EvPrepare](class.evprepare.md) викликані рівно перед стартом [Ev::run()](ev.run.md) таким чином, спостерігачі [EvPrepare](class.evprepare.md) є останніми викликаними спостерігачами перед тим, як цикл подій засне чи опитає нові події.

**`Ev::CHECK`**

Усі спостерігачі [EvCheck](class.evcheck.md) поміщені в чергу відразу після того, як [Ev::run()](ev.run.md) зібрав нові події, але до того, як вони викличуть якусь callback-функцію для отриманих подій. Таким чином, спостерігачі [EvCheck](class.evcheck.md) будуть викликані раніше, ніж будь-які інші спостерігачі з таким самим або нижчим пріоритетом у цій ітерації циклу подій.

**`Ev::EMBED`**

Вбудований цикл подій, заданий у спостерігачі [EvEmbed](class.evembed.md) вимагає себе уваги.

**`Ev::CUSTOM`**

Ніколи не надсилається (або іншим чином використовується) бібліотекою `libev` самостійно, але може вільно використовуватись користувачами `libev` для сигналізуючих спостерігачів (тобто за допомогою [EvWatcher::feed()](evwatcher.feed.md)

**`Ev::ERROR`**

Відбулася невідома помилка і спостерігача буде зупинено. Може статися через некоректний запуск спостерігача, тому що `libev` вичерпав ліміт по пам'яті, через закритий дескриптор файлу або з якоїсь ще причини . `Libev` вважає, що ці помилки програми. Також читайте розділ [» АНАТОМИЯ НАБЛЮДАТЕЛЕЙ](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#ANATOMY_OF_A_WATCHER_CONTENT)

Прапори бекенда:

**`Ev::BACKEND_SELECT`**

`выбор бэкенда - select(2)`

**`Ev::BACKEND_POLL`**

`опрос бэкенда - poll(2)`

**`Ev::BACKEND_EPOLL`**

Специфічний для Linux бекенд `epoll(7)` для ядер до та після 2.6.9

**`Ev::BACKEND_KQUEUE`**

`kqueue` - бекенде, що використовується в більшості систем BSD. Спостерігач [EvEmbed](class.evembed.md) може бути використаний для вставки одного циклу (з бекендом kqueue) в інший. Наприклад, можна спробувати створити цикл подій з бекендом `kqueue` та використовувати його тільки для сокетів.

**`Ev::BACKEND_DEVPOLL`**

Бекенд Solaris 8. Поки що не реалізований.

**`Ev::BACKEND_PORT`**

Механізм порту подій із гарним масштабуванням у Solaris 10.

**`Ev::BACKEND_ALL`**

Пробувати всі бекенди (крім зіпсованих). Не рекомендується використовувати безпосередньо. Тут потрібно використовувати побітові операції (тобто . **`Ev::BACKEND_ALL`** & ~ **`Ev::BACKEND_KQUEUE`** ). Використати [Ev::recommendedBackends()](ev.recommendedbackends.md) , або не ставити жодного бекенда взагалі.

**`Ev::BACKEND_MASK`**

Чи не бекенд, але маска для вибору всіх біт бекендів зі значення `flags`для виключення будь-яких бекендів. (тобто коли модифікуєте змінну оточення LIBEVFLAGS).

> **Зауваження**
> 
> Для циклу за замовчуванням, під час фази ініціалізації модуля `Ev`, реєструється виклик [» evloopfork](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#FUNCTIONS_CONTROLLING_EVENT_LOOPS_CO) за допомогою `pthread_atfork` (якщо такий є).

> **Зауваження**
> 
> Є методи, що дозволяють отримати доступ до *циклу подій за умовчанням* у класі **Єв** (наприклад, [Ev::iteration()](ev.iteration.md) [Ev::depth()](ev.depth.md) і т.д.). Для *користувальницьких циклів* (створених за допомогою **EvLoop:: construct()**) ці значення можуть бути доступні через відповідні властивості та методи класу [EvLoop](class.evloop.md)
> 
> Примірник циклу подій за умовчанням може бути вилучений за допомогою методу [EvLoop::defaultLoop()](evloop.defaultloop.md)

## Зміст

-   [Ev::backend](ev.backend.md) — Повертає ціле число, що описує бекенд, який використовується libev
-   [Ev::depth](ev.depth.md) — Здобути глибину рекурсії
-   [Ev::embeddableBackends](ev.embeddablebackends.md) — Повертає набір бекендів, які можна вбудувати в інші цикли подій
-   [Ev::feedSignal](ev.feedsignal.md) - Передаємо подію сигналу в Ev
-   [Ev::feedSignalEvent](ev.feedsignalevent.md) — Надіслати подію сигналу в цикл за замовчуванням
-   [Ev::iteration](ev.iteration.md) — Отримати кількість опитувань циклу за умовчанням щодо нових подій
-   [Ev::now](ev.now.md) — Отримати час запуску останньої ітерації циклу за умовчанням
-   [Ev::nowUpdate](ev.nowupdate.md) — Встановлює поточний час шляхом запиту до ядра в процесі оновлюючи час, який повертається Ev::now
-   [Ev::recommendedBackends](ev.recommendedbackends.md) — Отримати бітову маску рекомендованих бекендів для даної платформи
-   [Ev::resume](ev.resume.md) — Відновити виконання призупиненого раніше циклу подій за умовчанням
-   [Ev::run](ev.run.md) — Почати перевірку наявності подій та виклик callback-функцій циклу за умовчанням
-   [Ev::sleep](ev.sleep.md) — Блокувати процес задану кількість секунд
-   [Ev::stop](ev.stop.md) — Зупинити цикл події за замовчуванням
-   [Ev::supportedBackends](ev.supportedbackends.md) — Повертає набір бекендів, які підтримуються поточною конфігурацією libev
-   [Ev::suspend](ev.suspend.md) — Призупинити цикл подій за умовчанням
-   [Ev::time](ev.time.md) — Повертає поточний час у секундах (мільйонне число) минуле з початку епохи Unix
-   [Ev::verify](ev.verify.md) - Здійснює внутрішню перевірку цілісності (для налагодження)
