---
navigation:
  - function.passthru.md: « passthru
  - function.proc-get-status.md: proc\_get\_status »
  - index.md: PHP Manual
  - ref.exec.md: Функції запуску програм
title: proc\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# proc\_close

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

proc\_close — Завершити процес, відкритий [proc\_open()](function.proc-open.md) та повернути код повернення цього процесу

### Опис

```methodsynopsis
proc_close(resource $process): int
```

Функция**proc\_close()**похожа на функцию[pclose()](function.pclose.md), за винятком того, що вона працює тільки з процесами, відкритими за допомогою функції [proc\_open()](function.proc-open.md)Функция**proc\_close()** очікує завершення процесу та повертає його код повернення. Відкриті канали для цього процесу закриваються під час виклику цієї функції, щоб уникнути повної зупинки програми: дочірній процес не зможе завершитись, якщо є відкриті канали.

### Список параметрів

`process`

Дескриптор типу resource, відкритий за допомогою [proc\_open()](function.proc-open.md), що буде закрито.

### Значення, що повертаються

Повертає код завершення процесу, який було запущено. У разі помилки повертається `-1`

> **Зауваження** :
> 
> Якщо PHP зібрано з опцією --enable-sigchild, значення цієї функції, що повертається, не визначено.
