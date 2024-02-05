---
navigation:
  - reserved.variables.httpresponseheader.md: « $http\_response\_header
  - reserved.variables.argv.md: $argv »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $argc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $argc

(PHP 4, PHP 5, PHP 7, PHP 8)

$argc — Кількість аргументів, переданих скрипту

### Опис

Містить кількість аргументів, переданих поточному скрипту під час запуску [командного рядка](features.commandline.md)

> **Зауваження**: Ім'я файлу скрипта завжди передається як перший аргумент, таким чином мінімальне значення $argc одно

> **Зауваження**: Ця змінна недоступна, якщо [register\_argc\_argv](ini.core.md#ini.register-argc-argv) вимкнено.

### Приклади

**Приклад #1 Приклад використання $argc**

```php
<?php
var_dump($argc);
?>
```

Запустимо приклад у командному рядку: php script.php arg1 arg2 arg3

Висновок наведеного прикладу буде схожим на:

```
int(4)
```

### Примітки

> **Зауваження** :
> 
> Також доступно як [$\_SERVER\['argc'\]](reserved.variables.server.md)

### Дивіться також

-   [getopt()](function.getopt.md) \- Отримує параметри зі списку аргументів командного рядка
-   [](reserved.variables.argv.md)[$argv](reserved.variables.argv.md)
