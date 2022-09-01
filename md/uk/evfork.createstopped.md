---
navigation:
  - evfork.construct.md: '« EvFork::construct'
  - class.evidle.md: EvIdle »
  - index.md: PHP Manual
  - class.evfork.md: EvFork
title: 'EvFork::createStopped'
---
# EvFork::createStopped

(PECL ev >= 0.2.0)

EvFork::createStopped — Створити об'єкт класу EvFork, але не стартувати його

### Опис

```methodsynopsis
final
   public
   static
   EvFork::createStopped(
    string
     $callback
   , 
    string
     $data
    = ?, 
    string
     $priority
    = ?): object
```

Те саме, що й [EvFork::construct()](evfork.construct.md) але не виробляє автоматичного старту спостерігача.

### Список параметрів

`callback`

Дивіться [callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, асоційовані із спостерігачем

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт EvFork.

### Дивіться також

-   [EvFork::construct()](evfork.construct.md) - Конструктор спостерігача EvFork
