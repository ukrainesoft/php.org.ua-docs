---
navigation:
  - function.cli-get-process-title.html: « cligetprocesstitle
  - function.dl.html: dl »
  - index.html: PHP Manual
  - ref.info.html: Опції PHP/інформаційні функції
title: clisetprocesstitle
---
# clisetprocesstitle

(PHP 5> = 5.5.0, PHP 7, PHP 8)

clisetprocesstitle — Встановлює заголовок процесу

### Опис

```methodsynopsis
cli_set_process_title(string $title): bool
```

Встановлює заголовок процесу, видимий утилітами **top** і **пс**. Ця функція доступна лише в режимі [CLI](features.commandline.md)

### Список параметрів

`title`

Нове ім'я

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Якщо команда не підтримується вашою операційною системою, то буде викликана помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання **clisetprocesstitle()****

```php
<?php
$title = "Мой потрясающий PHP-скрипт";
$pid = getmypid(); // вы можете использовать это, чтобы увидеть заголовок процесса в ps

if (!cli_set_process_title($title)) {
    echo "Не удалось установить заголовок процесса для PID $pid...\n";
    exit(1);
} else {
    echo "Заголовок процесса '$title' для PID $pid был установлен!\n";
    sleep(5);
}
?>
```

### Дивіться також

-   [cligetprocesstitle()](function.cli-get-process-title.md) - Повертає заголовок поточного процесу
-   **setproctitle()**
