---
navigation:
  - function.cli-get-process-title.md: « cli\_get\_process\_title
  - function.dl.md: dl »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: cli\_set\_process\_title
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cli\_set\_process\_title

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

cli\_set\_process\_title — Встановлює заголовок процесу

### Опис

```methodsynopsis
cli_set_process_title(string $title): bool
```

Встановлює заголовок процесу, видимий утилітами **top**и**ps**. Ця функція доступна лише в режимі [CLI](features.commandline.md)

### Список параметрів

`title`

Нове ім'я

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо команда не підтримується вашою операційною системою, то буде викликана помилка рівня **`E_WARNING`**

### Приклади

**Пример #1 Пример использования**cli\_set\_process\_title()\*\*\*\*

```php
<?php
$title = "Мой потрясающий PHP-скрипт";
$pid = getmypid(); // вы можете использовать это, чтобы увидеть заголовок процесса в ps

if (!cli_set_process_title($title)) {
    echo "Не удалось установить заголовок процесса для PID $pid...\n";
    exit(1);
} else {
    echo "Заголовок процесса '$title' для PID $pid был установлен!\n";
    sleep(5);
}
?>
```

### Дивіться також

-   [cli\_get\_process\_title()](function.cli-get-process-title.md) \- Повертає заголовок поточного процесу
