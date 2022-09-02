---
navigation:
  - evcheck.construct.md: '« EvCheck::construct'
  - class.evchild.md: EvChild »
  - index.md: PHP Manual
  - class.evcheck.md: EvCheck
title: 'EvCheck::createStopped'
---
# EvCheck::createStopped

(PECL ev >= 0.2.0)

EvCheck::createStopped — Створює зупинений екземпляр спостерігача EvCheck

### Опис

```methodsynopsis
final
   public
   static
   EvCheck::createStopped(
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

Створює зупинений екземпляр спостерігача EvCheck.

### Список параметрів

`callback`

Дивіться [Callback-функції спостерігача](ev.watcher-callbacks.md)

`data`

Дані, пов'язані зі спостерігачем.

`priority`

[приоритет наблюдателя](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання повертає об'єкт EvCheck.

### Дивіться також

-   [EvPrepare](class.evprepare.md)
