Встановлює ідентифікатор групи процесу для менеджера завдань

-   [« posix\_setgid](function.posix-setgid.html)
    
-   [posix\_setrlimit »](function.posix-setrlimit.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Встановлює ідентифікатор групи процесу для менеджера завдань
    

# posixsetpgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixsetpgid - Встановлює ідентифікатор групи процесу для менеджера завдань

### Опис

```methodsynopsis
posix_setpgid(int $process_id, int $process_group_id): bool
```

Додає до процесу `process_id` ідентифікатор групи `process_group_id`

### Список параметрів

`process_id`

Ідентифікатор процесу.

`process_group_id`

Ідентифікатор групи процесу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   Для отримання більш повної інформації про процеси та керування завданнями зверніться до POSIX.1 та setsid(2) посібника в POSIX системах.