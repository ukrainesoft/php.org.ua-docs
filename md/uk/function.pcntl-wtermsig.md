Отримати сигнал, через який було примусово завершено дочірній процес

-   [« pcntl\_wstopsig](function.pcntl-wstopsig.html)
    
-   [POSIX »](book.posix.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCNTL](ref.pcntl.html)
    
-   Отримати сигнал, через який було примусово завершено дочірній процес
    

# pcntlwtermsig

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwtermsig — Отримати сигнал, через який було примусово завершено дочірній процес

### Опис

```methodsynopsis
pcntl_wtermsig(int $status): int|false
```

Повертає номер сигналу, через який примусово завершили дочірній процес. Має сенс тільки якщо [pcntl\_wifsignaled()](function.pcntl-wifsignaled.html) повернула **`true`**

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає номер сигналу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_signal()](function.pcntl-signal.html) - Встановлення оброблювача сигналу
-   [pcntl\_wifsignaled()](function.pcntl-wifsignaled.html) - Перевірити, чи код завершення процесу завершення по сигналу