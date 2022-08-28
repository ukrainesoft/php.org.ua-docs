Отримати сигнал, через який було зупинено дочірній процес

-   [« pcntl\_wifstopped](function.pcntl-wifstopped.html)
    
-   [pcntl\_wtermsig »](function.pcntl-wtermsig.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCNTL](ref.pcntl.html)
    
-   Отримати сигнал, через який було зупинено дочірній процес
    

# pcntlwstopsig

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwstopsig — Отримати сигнал, через який було зупинено дочірній процес

### Опис

```methodsynopsis
pcntl_wstopsig(int $status): int|false
```

Повертає сигнал, через який було зупинено дочірній процес. Функція має сенс лише якщо [pcntl\_wifstopped()](function.pcntl-wifstopped.html) повернула **`true`**

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає номер сигналу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_wifstopped()](function.pcntl-wifstopped.html) - Перевірити, чи зупинено дочірній процес