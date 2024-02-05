---
navigation:
  - function.proc-open.md: « proc\_open
  - function.shell-exec.md: shell\_exec »
  - index.md: PHP Manual
  - ref.exec.md: Функції запуску програм
title: proc\_terminate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# proc\_terminate

(PHP 5, PHP 7, PHP 8)

proc\_terminate — Знищити процес, відкритий за допомогою функції proc\_open

### Опис

```methodsynopsis
proc_terminate(resource $process, int $signal = 15): bool
```

Отправляет процессу`process`(созданному при помощи функции[proc\_open()](function.proc-open.md)) сигнал, який говорить про те, що він повинен завершитися. Функція **proc\_terminate()** повертається негайно і не очікує на завершення процесу.

Функция**proc\_terminate()** дозволяє завершити процес та продовжити виконання інших завдань. Ви можете опитувати процес (для того, щоб перевірити, чи він був завершений) за допомогою функції [proc\_get\_status()](function.proc-get-status.md)

### Список параметрів

`process`

Дескриптор типу resource, відкритий за допомогою функції [proc\_open()](function.proc-open.md), що буде закрито.

`signal`

Цей необов'язковий параметр корисний лише для операційних систем, які підтримують стандарт POSIX. Ви можете вказати сигнал, який буде надіслано процесу, використовуючи системний виклик `kill(2)`. За промовчанням використовується сигнал `SIGTERM`

### Значення, що повертаються

Повертає статус припинення процесу, який було запущено.

### Дивіться також

-   [proc\_open()](function.proc-open.md) \- Виконати команду та відкрити покажчик на файл для введення/виводу
-   [proc\_close()](function.proc-close.md) \- Завершити процес, відкритий proc\_open та повернути код повернення цього процесу
-   [proc\_get\_status()](function.proc-get-status.md) \- Отримати інформацію про процес, відкритий proc\_open
