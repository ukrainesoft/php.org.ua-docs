---
navigation:
  - function.phpversion.md: « phpversion
  - function.restore-include-path.md: restore\_include\_path »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: putenv
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# putenv

(PHP 4, PHP 5, PHP 7, PHP 8)

putenv — Встановлює значення змінного середовища

### Опис

```methodsynopsis
putenv(string $assignment): bool
```

Добавляет`assignment` у змінні оточення сервера. Змінна існуватиме лише на час виконання поточного запиту. Після його завершення змінна повернеться до початкового стану.

### Список параметрів

`assignment`

Установка вида`"FOO=BAR"`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Встановлення значення змінного середовища**

```php
<?php
putenv("UNIQID=$uniqid");
?>
```

### Дивіться також

-   [getenv()](function.getenv.md) \- набуває значення однієї чи всіх змінних оточення
-   [apache\_setenv()](function.apache-setenv.md) \- Встановлює змінну subprocess\_env Apache
