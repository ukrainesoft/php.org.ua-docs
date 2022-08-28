Надсилає сигнал відповідному процесу

-   [« posix\_isatty](function.posix-isatty.html)
    
-   [posix\_mkfifo »](function.posix-mkfifo.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Надсилає сигнал відповідному процесу
    

# posixkill

(PHP 4, PHP 5, PHP 7, PHP 8)

posixkill — Надсилає сигнал відповідному процесу

### Опис

```methodsynopsis
posix_kill(int $process_id, int $signal): bool
```

Надсилає сигнал `signal` процесу з ідентифікатором `process_id`

### Список параметрів

`process_id`

Ідентифікатор процесу.

`signal`

Одна з [PCNTL констант сигналов](pcntl.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   kill(2) посібник для POSIX систем, які містять додаткову інформацію про негативні ідентифікатори процесів, спеціальний ідентифікатор 0, спеціальний ідентифікатор -1, і сигнал з ідентифікатором 0.