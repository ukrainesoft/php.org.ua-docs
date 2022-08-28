Вказує, чи є файл каталогом

-   [« SplFileInfo::getType](splfileinfo.gettype.html)
    
-   [SplFileInfo::isExecutable »](splfileinfo.isexecutable.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Вказує, чи є файл каталогом
    

# SplFileInfo::isDir

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::isDir — Вказує, чи є файл каталогом

### Опис

```methodsynopsis
public SplFileInfo::isDir(): bool
```

Цей метод можна використовувати для визначення того, чи файл каталогом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо каталог; **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::isDir()****

```php
<?php
$d = new SplFileInfo(dirname(__FILE__));
var_dump($d->isDir());

$d = new SplFileInfo(__FILE__);
var_dump($d->isDir());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```