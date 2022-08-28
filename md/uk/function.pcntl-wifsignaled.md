Перевірити, чи відповідає код завершення процесу завершення сигналу

-   [« pcntl\_wifexited](function.pcntl-wifexited.html)
    
-   [pcntl\_wifstopped »](function.pcntl-wifstopped.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCNTL](ref.pcntl.html)
    
-   Перевірити, чи відповідає код завершення процесу завершення сигналу
    

# pcntlwifsignaled

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwifsignaled — Перевірити, чи код завершення процесу завершення по сигналу відповідає

### Опис

```methodsynopsis
pcntl_wifsignaled(int $status): bool
```

Перевірити, чи код завершення процесу завершення по сигналу.

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає **`true`**, якщо дочірній процес було завершено через неперехоплений сигнал. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_signal()](function.pcntl-signal.html) - Встановлення оброблювача сигналу