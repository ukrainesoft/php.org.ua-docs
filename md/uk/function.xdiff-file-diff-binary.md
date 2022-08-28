Псевдонім для xdifffilebdiff

-   [« xdiff\_file\_bpatch](function.xdiff-file-bpatch.html)
    
-   [xdiff\_file\_diff »](function.xdiff-file-diff.html)
    
-   [PHP Manual](index.html)
    
-   [Функции xdiff](ref.xdiff.html)
    
-   Псевдонім для xdifffilebdiff
    

# xdifffilediffbinary

(PECL xdiff >= 0.2.0)

xdifffilediffbinary - Псевдонім для xdifffilebdiff

### Опис

```methodsynopsis
xdiff_file_diff_binary(string $old_file, string $new_file, string $dest): bool
```

Створює файл бінарного патчу, порівнюючи два файли. Ця функція працює як з бінарними, так і текстовими файлами. Надалі отриманий патч можна застосувати за допомогою функцій [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.html)

Починаючи з версії 1.5.0, ця функція є псевдонімом [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.html)

### Список параметрів

`old_file`

Шлях до першого, "старого" файлу.

`new_file`

Шлях до другого, "нового" файлу.

`dest`

Шлях результуючого файлу патчу. Він міститиме різницю між старим і новим файлом у бінарному, людинонечитаемом.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Апмсер використання **xdifffilediffbinary()****

Наступний код створює бінарний патч, порівнюючи два архіви.

```php
<?php
$old_version = 'my_script_1.0.tgz';
$new_version = 'my_script_1.1.tgz';

xdiff_file_diff_binary($old_version, $new_version, 'my_script.bdiff');
?>
```

### Примітки

> **Зауваження**
> 
> Обидва файли будуть завантажені в пам'ять, тому переконайтеся, що параметр memorylimit налаштовано коректно.

### Дивіться також

-   [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.html) - Створити бінарний патч порівнюючи два файли
-   [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.html) - Застосувати бінарний патч до файлу