Отримання поточного значення конфігураційної установки includepath

-   [« get\_extension\_funcs](function.get-extension-funcs.html)
    
-   [get\_included\_files »](function.get-included-files.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Отримання поточного значення конфігураційної установки includepath
    

# getincludepath

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

getincludepath — Отримання поточного значення конфігураційної установки includepath

### Опис

```methodsynopsis
get_include_path(): string|false
```

Отримує значення налаштування конфігурації [include\_path](ini.core.html#ini.include-path)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу у вигляді рядка або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **getincludepath()****

```php
<?php
echo get_include_path();

// или используя ini_get()
echo ini_get('include_path');
?>
```

### Дивіться також

-   [ini\_get()](function.ini-get.html) - Отримує значення налаштування конфігурації
-   [restore\_include\_path()](function.restore-include-path.html) - Відновлює початкове значення конфігураційної установки includepath
-   [set\_include\_path()](function.set-include-path.html) - Встановлює налаштування конфігурації includepath
-   [include](function.include.html) - include