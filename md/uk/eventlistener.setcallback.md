---
navigation:
  - eventlistener.getsocketname.md: '« EventListener::getSocketName'
  - eventlistener.seterrorcallback.md: 'EventListener::setErrorCallback »'
  - index.md: PHP Manual
  - class.eventlistener.md: EventListener
title: 'EventListener::setCallback'
---
# EventListener::setCallback

(PECL event >= 1.2.6-beta)

EventListener::setCallback — Мета setCallback

### Опис

```methodsynopsis
public
   EventListener::setCallback(
    callable
     $cb
   , 
    mixed
     $arg
     = null
   ): void
```

Налаштуйте callback-функцію слухача події та, за необхідності, callback-аргумент.

### Список параметрів

`cb`

Нова callback-функція для нових підключень. Ігнорується, якщо **`null`**

Повинна відповідати прототипу:

```methodsynopsis
callback(    
       EventListener
        $listener
        = null
      ,    
       mixed
        $fd
        = null
      ,    
       array
        $address
        = null
      ,    
       mixed
        $arg
        = null
      ): void
```

`listener`

Об'єкт [EventListener](class.eventlistener.md)

`fd`

Файловий дескриптор чи ресурс, пов'язаний із слухачем.

`address`

Масив із двох елементів: IP-адреса та порт *server*

`arg`

Ці дані, прикріплені до callback-функції.

`arg`

Ці дані, прикріплені до callback-функції. Ігнорується, якщо **`null`**

### Значення, що повертаються

Функція не повертає значення після виконання.
