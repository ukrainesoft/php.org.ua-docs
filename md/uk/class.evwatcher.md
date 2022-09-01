---
navigation:
  - evtimer.set.html: '« EvTimer::set'
  - evwatcher.clear.html: 'EvWatcher::clear »'
  - index.html: PHP Manual
  - book.ev.html: Єв
title: Клас EvWatcher
---
# Клас EvWatcher

(PECL ev >= 0.2.0)

## Вступ

**EvWatcher** є базовим класом для всіх спостерігачів( [EvCheck](class.evcheck.html) [EvChild](class.evchild.html) і т.д.). Оскільки конструктор **EvWatcher** має модифікатор abstract, ви не повинні (і не зможете) створювати об'єкти цього класу безпосередньо.

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

ісactive

*Тільки читання*. Якщо спостерігач активний, то **`true`**, Якщо ні, то **`false`**

data

Довільні дані користувача.

ісpending

*Тільки читання*. якщо спостерігач у режимі очікування, тобто має нерозібрані повідомлення, а callback-функція ще не запускалася, то **`true`**. В іншому випадку **`false`**. Поки спостерігач перебуває в режимі очікування (але не активний), ви *не повинні* змінювати його пріоритет.

priority

Ціле число (int) в діапазоні від **`Ev::MINPRI`** до **`Ev::MAXPRI`**. Очікуючі спостерігачі з більш високим пріоритетом будуть викликані раніше спостерігачів з нижчим пріоритетом, але пріоритет не перешкоджатиме запуску спостерігача (за винятком спостерігачів [EvIdle](class.evidle.html)). Спостерігачі [EvIdle](class.evidle.html) надають функціонал, що запобігає виклику, якщо є очікувані високопріоритетні повідомлення.

## Зміст

-   [EvWatcher::clear](evwatcher.clear.html) — Очистити статус очікування спостерігача
-   [EvWatcher::construct](evwatcher.construct.html) - Абстрактний конструктор об'єкта спостерігача
-   [EvWatcher::feed](evwatcher.feed.html) — Подає зазначені події у цикл подій
-   [EvWatcher::getLoop](evwatcher.getloop.html) — Повертає цикл, який відповідає за спостерігача
-   [EvWatcher::invoke](evwatcher.invoke.html) - Викликає callback-функцію спостерігача із заданою бітовою маскою прийнятих подій
-   [EvWatcher::keepalive](evwatcher.keepalive.html) — Налаштовує, чи повертатиметься цикл
-   [EvWatcher::setCallback](evwatcher.setcallback.html) - Встановлює нову callback-функцію для спостерігача
-   [EvWatcher::start](evwatcher.start.html) - Запускає спостерігача
-   [EvWatcher::stop](evwatcher.stop.html) - Зупиняє спостерігача
