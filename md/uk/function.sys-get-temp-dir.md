Повертає шлях до директорії тимчасових файлів

-   [« settimelimit](function.set-time-limit.html)
    
-   [versioncompare »](function.version-compare.html)
    
-   [PHP Manual](index.html)
    
-   [Опції PHP/інформаційні функції](ref.info.html)
    
-   Повертає шлях до директорії тимчасових файлів
    

# sysgettempdir

(PHP 5> = 5.2.1, PHP 7, PHP 8)

sysgettempdir — Повертає шлях до директорії тимчасових файлів

### Опис

```methodsynopsis
sys_get_temp_dir(): string
```

Повертає шлях до директорії, де PHP за замовчуванням зберігає тимчасові файли.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до директорії тимчасових файлів.

### Приклади

**Приклад #1 Приклад використання **sysgettempdir()****

```php
<?php
// Создание временного файла в директории
// временных файлов, используя sys_get_temp_dir()
$temp_file = tempnam(sys_get_temp_dir(), 'Tux');

echo $temp_file;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
C:\Windows\Temp\TuxA318.tmp
```

### Дивіться також

-   [tmpfile()](function.tmpfile.html) - Створює тимчасовий файл
-   [tempnam()](function.tempnam.html) - Створює файл із унікальним ім'ям