Знищити процес, відкритий за допомогою функції procopen

-   [« procopen](function.proc-open.html)
    
-   [shellexec »](function.shell-exec.html)
    
-   [PHP Manual](index.html)
    
-   [Функции запуска программ](ref.exec.html)
    
-   Знищити процес, відкритий за допомогою функції procopen
    

# procterminate

(PHP 5, PHP 7, PHP 8)

procterminate — Знищити процес, відкритий за допомогою функції procopen

### Опис

```methodsynopsis
proc_terminate(resource $process, int $signal = 15): bool
```

Відправляє процесу `process` (створеному за допомогою функції [procopen()](function.proc-open.html)) сигнал, який говорить про те, що він повинен завершитися. Функція **procterminate()** повертається негайно і не очікує на завершення процесу.

Функція **procterminate()** дозволяє завершити процес та продовжити виконання інших завдань. Ви можете опитувати процес (для того, щоб перевірити, чи він був завершений) за допомогою функції [procgetstatus()](function.proc-get-status.html)

### Список параметрів

`process`

Дескриптор типу resource, відкритий за допомогою функції [procopen()](function.proc-open.html), який буде закрито.

`signal`

Цей необов'язковий параметр корисний лише для операційних систем, які підтримують POSIX. Ви можете вказати сигнал, який буде надіслано процесу, використовуючи системний виклик `kill(2)`. За промовчанням використовується сигнал `SIGTERM`

### Значення, що повертаються

Повертає статус припинення процесу, який було запущено.

### Дивіться також

-   [procopen()](function.proc-open.html) - Виконати команду та відкрити покажчик на файл для введення/виводу
-   [procclose()](function.proc-close.html) - Завершити процес, відкритий procopen та повернути код повернення цього процесу
-   [procgetstatus()](function.proc-get-status.html) - Отримати інформацію про процес, відкритий procopen