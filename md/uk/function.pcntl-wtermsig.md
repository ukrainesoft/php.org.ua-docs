Отримати сигнал, через який було примусово завершено дочірній процес

-   [pcntlwstopsig](function.pcntl-wstopsig.html)
    
-   [POSIX »](book.posix.md)
    
-   [PHP Manual](index.md)
    
-   [Функції PCNTL](ref.pcntl.md)
    
-   Отримати сигнал, через який було примусово завершено дочірній процес
    

# pcntlwtermsig

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwtermsig — Отримати сигнал, через який було примусово завершено дочірній процес

### Опис

```methodsynopsis
pcntl_wtermsig(int $status): int|false
```

Повертає номер сигналу, через який примусово завершили дочірній процес. Має сенс тільки якщо [pcntlwifsignaled()](function.pcntl-wifsignaled.html) повернула **`true`**

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає номер сигналу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlsignal()](function.pcntl-signal.html) - Встановлення оброблювача сигналу
-   [pcntlwifsignaled()](function.pcntl-wifsignaled.html) - Перевірити, чи код завершення процесу завершення по сигналу