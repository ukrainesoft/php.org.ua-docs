Встановлює значення конфігураційної установки includepath

-   [« restore\_include\_path](function.restore-include-path.html)
    
-   [set\_time\_limit »](function.set-time-limit.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Встановлює значення конфігураційної установки includepath
    

# setincludepath

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

setincludepath — Встановлює налаштування конфігурації includepath

### Опис

```methodsynopsis
set_include_path(string $include_path): string|false
```

Задає значення конфігураційної установки [include\_path](ini.core.html#ini.include-path) тимчасово виконання скрипта.

### Список параметрів

`include_path`

Нове значення налаштування [include\_path](ini.core.html#ini.include-path)

### Значення, що повертаються

Повертає старе значення [include\_path](ini.core.html#ini.include-path) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **setincludepath()****

```php
<?php
set_include_path('/usr/lib/pear');

// Или так
ini_set('include_path', '/usr/lib/pear');
?>
```

**Приклад #2 Упорядкування більш довгого шляху include path**

Використовуючи константу **`PATH_SEPARATOR`**, можна додати до шляху вкладені директорії незалежно від операційної системи.

У цьому прикладі ми додамо /usr/lib/pear до кінця існуючого шляху `include_path`

```php
<?php
$path = '/usr/lib/pear';
set_include_path(get_include_path() . PATH_SEPARATOR . $path);
?>
```

### Дивіться також

-   [ini\_set()](function.ini-set.html) - Встановлює налаштування конфігурації
-   [get\_include\_path()](function.get-include-path.html) - Отримання поточного значення конфігураційної установки includepath
-   [restore\_include\_path()](function.restore-include-path.html) - Відновлює початкове значення конфігураційної установки includepath
-   [include](function.include.html) - include