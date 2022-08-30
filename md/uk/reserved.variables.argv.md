Масив переданих скрипту аргументів

-   [« $argc](reserved.variables.argc.html)
    
-   [Предопределённые исключения »](reserved.exceptions.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые переменные](reserved.variables.html)
    
-   Масив переданих скрипту аргументів
    

# $argv

(PHP 4, PHP 5, PHP 7, PHP 8)

$argv — Масив переданих скрипту аргументів

### Опис

Містить масив (array) всіх аргументів, переданих скрипту при запуску з [командного рядка](features.commandline.html)

> **Зауваження**: Перший аргумент $argv завжди містить ім'я запущеного файлу скрипта.

> **Зауваження**: Ця змінна недоступна, якщо [registerargcargv](ini.core.html#ini.register-argc-argv) вимкнено.

### Приклади

**Приклад #1 Приклад використання $argv**

```php
<?php
var_dump($argv);
?>
```

Запустимо приклад у командному рядку: php script.php arg1 arg2 arg3

Результатом виконання цього прикладу буде щось подібне:

```
array(4) {
  [0]=>
  string(10) "script.php"
  [1]=>
  string(4) "arg1"
  [2]=>
  string(4) "arg2"
  [3]=>
  string(4) "arg3"
}
```

### Примітки

> **Зауваження**
> 
> Також доступно як [SERVER\['argv'\]](reserved.variables.server.html)

### Дивіться також

-   [getopt()](function.getopt.html) - Отримує параметри зі списку аргументів командного рядка
-   [](reserved.variables.argc.html)[$argc](reserved.variables.argc.html)