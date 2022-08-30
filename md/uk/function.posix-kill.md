Надсилає сигнал відповідному процесу

-   [« posixisatty](function.posix-isatty.html)
    
-   [posixmkfifo »](function.posix-mkfifo.html)
    
-   [PHP Manual](index.md)
    
-   [POSIX Функции](ref.posix.md)
    
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

Одна з [PCNTL констант сигналів](pcntl.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   kill(2) посібник для POSIX систем, які містять додаткову інформацію про негативні ідентифікатори процесів, спеціальний ідентифікатор 0, спеціальний ідентифікатор -1, і сигнал з ідентифікатором 0.