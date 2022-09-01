---
navigation:
  - function.proc-open.html: « procopen
  - function.shell-exec.html: shellexec »
  - index.md: PHP Manual
  - ref.exec.md: Функции запуска программ
title: procterminate
---
# procterminate

(PHP 5, PHP 7, PHP 8)

procterminate — Знищити процес, відкритий за допомогою функції procopen

### Опис

```methodsynopsis
proc_terminate(resource $process, int $signal = 15): bool
```

Відправляє процесу `process` (створеному за допомогою функції [procopen()](function.proc-open.md)) сигнал, який говорить про те, що він повинен завершитися. Функція **procterminate()** повертається негайно і не очікує на завершення процесу.

Функція **procterminate()** дозволяє завершити процес та продовжити виконання інших завдань. Ви можете опитувати процес (для того, щоб перевірити, чи він був завершений) за допомогою функції [procgetstatus()](function.proc-get-status.md)

### Список параметрів

`process`

Дескриптор типу resource, відкритий за допомогою функції [procopen()](function.proc-open.md), який буде закрито.

`signal`

Цей необов'язковий параметр корисний лише для операційних систем, які підтримують POSIX. Ви можете вказати сигнал, який буде надіслано процесу, використовуючи системний виклик `kill(2)`. За промовчанням використовується сигнал `SIGTERM`

### Значення, що повертаються

Повертає статус припинення процесу, який було запущено.

### Дивіться також

-   [procopen()](function.proc-open.md) - Виконати команду та відкрити покажчик на файл для введення/виводу
-   [procclose()](function.proc-close.md) - Завершити процес, відкритий procopen та повернути код повернення цього процесу
-   [procgetstatus()](function.proc-get-status.md) - Отримати інформацію про процес, відкритий procopen
