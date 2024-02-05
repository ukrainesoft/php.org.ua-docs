---
navigation:
  - evfork.construct.md: '« EvFork::\_\_construct'
  - class.evidle.md: EvIdle »
  - index.md: PHP Manual
  - class.evfork.md: EvFork
title: 'EvFork::createStopped'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Те саме, що й [EvFork::\_\_construct()](evfork.construct.md) але не виробляє автоматичного старту спостерігача.

### Список параметрів

`callback`

Смотрите[callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, асоційовані із спостерігачем

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт EvFork.

### Дивіться також

-   [EvFork::\_\_construct()](evfork.construct.md) \- Конструктор спостерігача EvFork
