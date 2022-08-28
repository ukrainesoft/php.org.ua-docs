Отримує інформацію про файл

-   [« SplFileObject::fseek](splfileobject.fseek.html)
    
-   [SplFileObject::ftell »](splfileobject.ftell.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Отримує інформацію про файл
    

# SplFileObject::fstat

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::fstat — Отримує інформацію про файл

### Опис

```methodsynopsis
public SplFileObject::fstat(): array
```

Збирає статистичну інформацію про файл. Поведінка ідентична [fstat()](function.fstat.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив зі статистичною інформацією про файл; формат масиву докладно описано на сторінці функції [stat()](function.stat.html)

### Приклади

**Приклад #1 Приклад використання **SplFileObject::fstat()****

```php
<?php
$file = new SplFileObject("/etc/passwd");
$stat = $file->fstat();

// Печать только ассоциативной части
print_r(array_slice($stat, 13));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [dev] => 771
    [ino] => 488704
    [mode] => 33188
    [nlink] => 1
    [uid] => 0
    [gid] => 0
    [rdev] => 0
    [size] => 1114
    [atime] => 1061067181
    [mtime] => 1056136526
    [ctime] => 1056136526
    [blksize] => 4096
    [blocks] => 8
)
```

### Дивіться також

-   [fstat()](function.fstat.html) - Отримує інформацію про файл, використовуючи відкритий файловий покажчик
-   [stat()](function.stat.html) - Повертає інформацію про файл