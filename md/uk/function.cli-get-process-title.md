---
navigation:
  - function.assert.md: « assert
  - function.cli-set-process-title.md: cli\_set\_process\_title »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: cli\_get\_process\_title
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cli\_get\_process\_title

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

cli\_get\_process\_title — Повертає заголовок поточного процесу

### Опис

```methodsynopsis
cli_get_process_title(): ?string
```

Повертає заголовок поточного процесу, встановлений [cli\_set\_process\_title()](function.cli-set-process-title.md). Зауважте, що залежно від вашої операційної системи, це ім'я може не збігатися з тим, що покажуть утиліти **ps** і **top**

Ця функція доступна лише в режимі [CLI](features.commandline.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверне рядок із заголовком процесу або \*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Якщо команда не підтримується вашою операційною системою, то буде викликана помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання** cli\_get\_process\_title()\*\*\*\*

```php
<?php
echo "Заголовок процесса: " . cli_get_process_title() . "\n";
?>
```

### Дивіться також

-   [cli\_set\_process\_title()](function.cli-set-process-title.md) \- Встановлює заголовок процесу
