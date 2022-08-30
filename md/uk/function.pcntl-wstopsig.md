Отримати сигнал, через який було зупинено дочірній процес

-   [pcntlwifstopped](function.pcntl-wifstopped.html)
    
-   [pcntlwtermsig »](function.pcntl-wtermsig.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PCNTL](ref.pcntl.html)
    
-   Отримати сигнал, через який було зупинено дочірній процес
    

# pcntlwstopsig

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwstopsig — Отримати сигнал, через який було зупинено дочірній процес

### Опис

```methodsynopsis
pcntl_wstopsig(int $status): int|false
```

Повертає сигнал, через який було зупинено дочірній процес. Функція має сенс лише якщо [pcntlwifstopped()](function.pcntl-wifstopped.html) повернула **`true`**

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає номер сигналу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlwifstopped()](function.pcntl-wifstopped.html) - Перевірити, чи зупинено дочірній процес