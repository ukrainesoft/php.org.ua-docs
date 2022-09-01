---
navigation:
  - eventutil.getsocketfd.md: '« EventUtil::getSocketFd'
  - eventutil.setsocketoption.md: 'EventUtil::setSocketOption »'
  - index.md: PHP Manual
  - class.eventutil.md: EventUtil
title: 'EventUtil::getSocketName'
---
# EventUtil::getSocketName

(PECL event >= 1.5.0)

EventUtil::getSocketName — Отримати поточну адресу, до якої прив'язаний сокет

### Опис

```methodsynopsis
public
   static
   EventUtil::getSocketName(
    mixed
     $socket
   , 
    string
     &$address
   , 
    mixed
     &$port
    = ?): bool
```

Повертає поточну адресу, до якої прив'язаний сокет `socket`

### Список параметрів

`socket`

Ресурс сокету, потоку чи файловий дескриптор, пов'язаний із сокетом.

`address`

Вихідний параметр. IP-адреса або шлях до доменного сокету UNIX.

`port`

Вихідний параметр. Порт, якого прив'язаний сокет. Немає сенсу для доменних сокетів UNIX.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
