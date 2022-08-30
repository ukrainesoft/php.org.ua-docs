Перевірити, чи відповідає код завершення процесу завершення сигналу

-   [pcntlwifexited](function.pcntl-wifexited.html)
    
-   [pcntlwifstopped »](function.pcntl-wifstopped.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PCNTL](ref.pcntl.md)
    
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

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає **`true`**, якщо дочірній процес було завершено через неперехоплений сигнал. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlsignal()](function.pcntl-signal.html) - Встановлення оброблювача сигналу