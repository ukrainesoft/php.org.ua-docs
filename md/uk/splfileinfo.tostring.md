Повертає шлях до файлу у вигляді рядка

-   [« SplFileInfo::setInfoClass](splfileinfo.setinfoclass.md)
    
-   [SplFileObject »](class.splfileobject.md)
    
-   [PHP Manual](index.md)
    
-   [SplFileInfo](class.splfileinfo.md)
    
-   Повертає шлях до файлу у вигляді рядка
    

# SplFileInfo::toString

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::toString — Повертає шлях до файлу у вигляді рядка

### Опис

```methodsynopsis
public SplFileInfo::__toString(): string
```

Цей метод поверне ім'я цього файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::toString()****

```php
<?php
$info = new SplFileInfo('foo');
var_dump($info->__toString());
echo $info.PHP_EOL;

$info = new SplFileInfo('/usr/bin/php');
var_dump($info->__toString());
echo $info.PHP_EOL;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(3) "foo"
foo
string(12) "/usr/bin/php"
/usr/bin/php
```