---
navigation:
  - event.pending.md: '« Event::pending'
  - event.setpriority.md: 'Event::setPriority »'
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Event::set

(PECL event >= 1.2.6-beta)

Event::set — Переконфігурувати подію

### Опис

```methodsynopsis
public
   Event::set(    
    EventBase
     $base
   ,    
    mixed
     $fd
   ,    
    int
     $what
    = ?,    
    callable
     $cb
    = ?,    
    mixed
     $arg
    = ?): bool
```

Переконфігурує подію. Зверніть увагу, що ця функція не викликає застарілої функції event\_set бібліотеки libevent. Натомість вона викликає event\_assign.

### Список параметрів

`base`

Подієва база, до якої необхідно прив'язати подію.

`fd`

Потік, сокет чи числовий дескриптор файлу. Для подій таймера вкажіть **`-1`**, а для подій сигналу - номер сигналу, наприклад **`SIGHUP`**

`what`

Смотрите[Прапори подій](event.flags.md)

`cb`

Функція зворотного дзвінка. Дивіться [Функції зворотного дзвінка для подій](event.callbacks.md)

`arg`

Ці дані, пов'язані з подією. Вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
