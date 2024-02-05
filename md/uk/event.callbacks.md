---
navigation:
  - event.persistence.md: « Про постійні (persistent) події
  - event.constructing.signal.events.md: Створення подій для сигналів »
  - index.md: PHP Manual
  - book.event.md: Event
title: Callback-функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Callback-функції

Якщо для події зареєстрована callback-функція, вона буде викликана, коли подія перейде в активний статус. Для прив'язування функції до події необхідно передати її як параметр [callable](language.types.callable.md)в[Event::\_\_construct()](event.construct.md) або [Event::set()](event.set.md) або в один із фабричних методів, таких як [Event::timer()](event.timer.md)

Функція повинна відповідати наступному прототипу:

```methodsynopsis
callback(
   mixed
     $fd
     = null
  , 
   int
     $what
   = ?, 
   mixed
     $arg
     = null
  ): void
```

`fd`

Дескриптор файлу, потокового ресурсу чи сокету, пов'язані з подією. Для подій сигналів `fd` збігається із номером сигналу.

`what`

Побітова маска *всіх* оброблюваних подій.

`arg`

Дані користувача.

Для[Event::timer()](event.timer.md)callback-функция должна соответствовать следующему прототипу:

```methodsynopsis
callback(
   mixed
     $arg
     = null
  ): void
```

`arg`

Дані користувача.

Для[Event::signal()](event.signal.md)callback-функция должна соответствовать следующему прототипу:

```methodsynopsis
callback(
   int
     $signum
   = ?, 
   mixed
     $arg
     = null
  ): void
```

`signum`

Номер сигналу (наприклад, **`SIGTERM`**

`arg`

Дані користувача.
