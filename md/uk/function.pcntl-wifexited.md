Перевіряє, чи код завершення процесу відповідає нормальному завершенню.

-   [« pcntl\_wexitstatus](function.pcntl-wexitstatus.html)
    
-   [pcntl\_wifsignaled »](function.pcntl-wifsignaled.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCNTL](ref.pcntl.html)
    
-   Перевіряє, чи код завершення процесу відповідає нормальному завершенню.
    

# pcntlwifexited

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwifexited — Перевіряє, чи код завершення процесу відповідає нормальному завершенню.

### Опис

```methodsynopsis
pcntl_wifexited(int $status): bool
```

Перевіряє, чи код завершення процесу відповідає нормальному завершенню.

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає **`true`**якщо код завершення дочірнього процесу відповідає нормальному завершенню. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_wexitstatus()](function.pcntl-wexitstatus.html) - Отримати код повернення завершеного дочірнього процесу