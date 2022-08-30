Встановлює значення змінного середовища

-   [« phpversion](function.phpversion.html)
    
-   [restoreincludepath »](function.restore-include-path.html)
    
-   [PHP Manual](index.html)
    
-   [Опції PHP/інформаційні функції](ref.info.html)
    
-   Встановлює значення змінного середовища
    

# putenv

(PHP 4, PHP 5, PHP 7, PHP 8)

putenv — Встановлює значення змінного середовища

### Опис

```methodsynopsis
putenv(string $assignment): bool
```

Додає `assignment` у змінні оточення сервера. Змінна існуватиме лише на час виконання поточного запиту. Після його завершення змінна повернеться до початкового стану.

### Список параметрів

`assignment`

Встановлення виду `"FOO=BAR"`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Установка значення змінного середовища**

```php
<?php
putenv("UNIQID=$uniqid");
?>
```

### Дивіться також

-   [getenv()](function.getenv.html) - набуття значення змінної оточення
-   [apachesetenv()](function.apache-setenv.html) - Встановлює змінну subprocessenv Apache