---
navigation:
  - evtimer.set.md: '« EvTimer::set'
  - evwatcher.clear.md: 'EvWatcher::clear »'
  - index.md: PHP Manual
  - book.ev.md: Ev
title: Клас EvWatcher
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EvWatcher

(PECL ev >= 0.2.0)

## Вступ

**EvWatcher** є базовим класом для всіх спостерігачів( [EvCheck](class.evcheck.md) [EvChild](class.evchild.md) і т.д.). Оскільки конструктор **EvWatcher** має модифікатор abstract, ви не повинні (і не зможете) створювати об'єкти цього класу безпосередньо.

## Огляд класів

```classsynopsis

     
    
    
    
     
      abstract
      class EvWatcher
     
     {
    
    /* Свойства */
    
     public
      $is_active;

    public
      $data;

    public
      $is_pending;

    public
      $priority;

    /* Методы */
    
   abstract
   public
   __construct()

    public
   clear(): int
public
   feed(
    int
     $revents
   ): void
public
   getLoop(): EvLoop
public
   invoke(
    int
     $revents
   ): void
public
   keepalive(
    bool
     $value
    = ?): bool
public
   setCallback(
    callable
     $callback
   ): void
public
   start(): void
public
   stop(): void

   }
```

## Властивості

is\_active

*Тільки читання*. Якщо спостерігач активний, то **`true`**, Якщо ні, то **`false`**

data

Довільні дані користувача.

is\_pending

*Тільки читання*. якщо спостерігач у режимі очікування, тобто має нерозібрані повідомлення, а callback-функція ще не запускалася, то **`true`**. В іншому випадку **`false`**. Поки спостерігач перебуває в режимі очікування (але не активний), ви *не повинні* змінювати його пріоритет.

priority

Целое число (int) в диапазоне от\*\*`Ev::MINPRI`**до**`Ev::MAXPRI`\*\*. Очікуючі спостерігачі з більш високим пріоритетом будуть викликані раніше спостерігачів з нижчим пріоритетом, але пріоритет не перешкоджатиме запуску спостерігача (за винятком спостерігачів [EvIdle](class.evidle.md)). Спостерігачі [EvIdle](class.evidle.md) надають функціонал, що запобігає виклику, якщо є очікувані високопріоритетні повідомлення.

## Зміст

-   [EvWatcher::clear](evwatcher.clear.md)— Очистити статус очікування спостерігача
-   [EvWatcher::\_\_construct](evwatcher.construct.md) \- Абстрактний конструктор об'єкта спостерігача
-   [EvWatcher::feed](evwatcher.feed.md)— Подає зазначені події у цикл подій
-   [EvWatcher::getLoop](evwatcher.getloop.md)— Повертає цикл, який відповідає за спостерігача
-   [EvWatcher::invoke](evwatcher.invoke.md) \- Викликає callback-функцію спостерігача із заданою бітовою маскою прийнятих подій
-   [EvWatcher::keepalive](evwatcher.keepalive.md)— Налаштовує, чи повертатиметься цикл
-   [EvWatcher::setCallback](evwatcher.setcallback.md) \- Встановлює нову callback-функцію для спостерігача
-   [EvWatcher::start](evwatcher.start.md) \- Запускає спостерігача
-   [EvWatcher::stop](evwatcher.stop.md) \- Зупиняє спостерігача
