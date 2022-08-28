Вказує, чи є файл посиланням

-   [« SplFileInfo::isFile](splfileinfo.isfile.html)
    
-   [SplFileInfo::isReadable »](splfileinfo.isreadable.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Вказує, чи є файл посиланням
    

# SplFileInfo::isLink

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::isLink — Вказує, чи є файл посиланням

### Опис

```methodsynopsis
public SplFileInfo::isLink(): bool
```

Використовуйте цей метод, щоб перевірити, чи є файл, на який посилається об'єкт SplFileInfo, посиланням.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**якщо файл є посиланням; **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::isLink()****

```php
<?php
$info = new SplFileInfo('/path/to/symlink');
if ($info->isLink()) {
    echo 'Реальный путь: '.$info->getRealPath();
}
?>
```

### Дивіться також

-   [SplFileInfo::getRealPath()](splfileinfo.getrealpath.html) - Отримує абсолютний шлях до файлу