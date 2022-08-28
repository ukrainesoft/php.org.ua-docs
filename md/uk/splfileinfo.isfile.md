Вказує, чи об'єкт посилається на звичайний файл

-   [« SplFileInfo::isExecutable](splfileinfo.isexecutable.html)
    
-   [SplFileInfo::isLink »](splfileinfo.islink.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Вказує, чи об'єкт посилається на звичайний файл
    

# SplFileInfo::isFile

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::isFile — Вказує, чи об'єкт посилається на звичайний файл

### Опис

```methodsynopsis
public SplFileInfo::isFile(): bool
```

Перевіряє, чи існує файл, на який посилається об'єкт SplFileInfo, і чи він є звичайним файлом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо файл існує і є звичайним файлом (а не посиланням), **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::isFile()****

```php
<?php
$info = new SplFileInfo(__FILE__);
var_dump($info->isFile());

$info = new SplFileInfo(dirname(__FILE__));
var_dump($info->isFile());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```