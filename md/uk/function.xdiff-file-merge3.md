Об'єднання трьох файлів в один

-   [xdifffilediff](function.xdiff-file-diff.html)
    
-   [xdifffilepatchbinary »](function.xdiff-file-patch-binary.html)
    
-   [PHP Manual](index.html)
    
-   [Функції xdiff](ref.xdiff.html)
    
-   Об'єднання трьох файлів в один
    

# xdifffilemerge3

(PECL xdiff >= 0.2.0)

xdifffilemerge3 - Об'єднання трьох файлів в один

### Опис

```methodsynopsis
xdiff_file_merge3(    string $old_file,    string $new_file1,    string $new_file2,    string $dest): mixed
```

Об'єднує три файли в один і зберігає результат у `dest`. Файл `old_file` є оригінальним файлом, тоді як `new_file1` і `new_file2` його модифікованими версіями.

### Список параметрів

`old_file`

Шлях до першого, "старого" файлу.

`new_file1`

Шлях до другого файлу. Модифікованої версії `old_file`

`new_file2`

Шлях до третього файлу. Модифікованої версії `old_file`

`dest`

Шлях до результуючого файлу, який міститиме об'єднані зміни з `new_file1` і `new_file2`

### Значення, що повертаються

Повертає **`true`**, якщо об'єднання пройшло успішно, рядок з відхиленими даними, якщо ні, та **`false`** у разі внутрішньої помилки.

### Приклади

**Приклад #1 Приклад використання **xdifffilemerge3()****

Наступний код поєднує три файли.

```php
<?php
$old_version = 'original_script.php';
$fix1 = 'script_with_fix1.php';
$fix2 = 'script_with_fix2.php';

$errors = xdiff_file_merge3($old_version, $fix1, $fix2, 'fixed_script.php');
if (is_string($errors)) {
    echo "Отклонены:\n";
    echo $errors;
}
?>
```

### Дивіться також

-   [xdiffstringmerge3()](function.xdiff-string-merge3.html) - Об'єднати три рядки в один