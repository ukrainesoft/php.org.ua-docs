---
navigation:
  - event.deltimer.md: '« Event::delTimer'
  - event.getsupportedmethods.md: 'Event::getSupportedMethods »'
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::free'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Event::free

(PECL event >= 1.2.6-beta)

Event::free — Перевести подію в пасивний стан і звільнити всі виділені для неї ресурси

### Опис

```methodsynopsis
public
   Event::free(): void
```

Видаляє подію з набору відстежуваних libevent подій і звільняє всі виділені йому ресурси.

**Увага**

В настоящее время метод**Event::free()** не знищує сам об'єкт. Для знищення об'єкта події використовуйте функцію [unset()](function.unset.md)или присвойте ему\*\*`null`\*\*

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Event::\_\_construct()](event.construct.md) \- Конструктор об'єкту Event
