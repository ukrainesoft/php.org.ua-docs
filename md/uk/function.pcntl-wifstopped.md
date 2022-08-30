Перевірити, чи зупинено дочірній процес

-   [pcntlwifsignaled](function.pcntl-wifsignaled.html)
    
-   [pcntlwstopsig »](function.pcntl-wstopsig.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PCNTL](ref.pcntl.html)
    
-   Перевірити, чи зупинено дочірній процес
    

# pcntlwifstopped

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwifstopped — Перевірити, чи зупинено дочірній процес

### Опис

```methodsynopsis
pcntl_wifstopped(int $status): bool
```

Перевіряє, чи зупинено дочірній процес, що викликало повернення; це можливо лише якщо функція [pcntlwaitpid()](function.pcntl-waitpid.html) викликалася з опцією `WUNTRACED`

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо дочірній процес викликав повернення зараз зупинено. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу