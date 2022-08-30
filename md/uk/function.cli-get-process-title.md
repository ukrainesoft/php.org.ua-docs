Повертає заголовок поточного процесу

-   [« assert](function.assert.md)
    
-   [clisetprocesstitle »](function.cli-set-process-title.html)
    
-   [PHP Manual](index.md)
    
-   [Опції PHP/інформаційні функції](ref.info.md)
    
-   Повертає заголовок поточного процесу
    

# cligetprocesstitle

(PHP 5> = 5.5.0, PHP 7, PHP 8)

cligetprocesstitle — Повертає заголовок поточного процесу

### Опис

```methodsynopsis
cli_get_process_title(): ?string
```

Повертає заголовок поточного процесу, встановлений [clisetprocesstitle()](function.cli-set-process-title.html). Зауважте, що залежно від вашої операційної системи, це ім'я може не збігатися з тим, що покажуть утиліти **пс** і **top**

Ця функція доступна лише в режимі [CLI](features.commandline.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверне рядок із заголовком процесу або **`null`** у разі виникнення помилки.

### Помилки

Якщо команда не підтримується вашою операційною системою, то буде викликана помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання **cligetprocesstitle()****

```php
<?php
echo "Заголовок процесса: " . cli_get_process_title() . "\n";
?>
```

### Дивіться також

-   [clisetprocesstitle()](function.cli-set-process-title.html) - Встановлює заголовок процесу