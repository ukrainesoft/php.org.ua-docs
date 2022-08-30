Псевдонім для xdifffilebpatch

-   [xdifffilemerge3](function.xdiff-file-merge3.html)
    
-   [xdifffilepatch »](function.xdiff-file-patch.html)
    
-   [PHP Manual](index.html)
    
-   [Функції xdiff](ref.xdiff.html)
    
-   Псевдонім для xdifffilebpatch
    

# xdifffilepatchbinary

(PECL xdiff >= 0.2.0)

xdifffilepatchbinary - Псевдонім для xdifffilebpatch

### Опис

```methodsynopsis
xdiff_file_patch_binary(string $file, string $patch, string $dest): bool
```

Застосувати до файлу `file` патч `patch` і записати результат у файл `dest`. Ця функція приймає патчі створені як [xdifffilebdiff()](function.xdiff-file-bdiff.html) так і [xdifffilerabdiff()](function.xdiff-file-rabdiff.html) або їх копії.

Починаючи з версії 1.5.0, ця функція є псевдонімом [xdifffilebpatch()](function.xdiff-file-bpatch.html)

### Список параметрів

`file`

Оригінальний файл.

`patch`

Файл бінарний патч.

`dest`

Підсумковий файл.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **xdifffilepatchbinary()****

У наступному коді показано застосування бінарного патчу до файлу.

```php
<?php
$old_version = 'archive-1.0.tgz';
$patch = 'archive.bpatch';

$result = xdiff_file_patch_binary($old_version, $patch, 'archive-1.1.tgz');
if ($result) {
   echo "Файл пропатчен";
} else {
   echo "Файл не может быть пропатчен";
}

?>
```

### Примітки

> **Зауваження**
> 
> Обидва файли (`file` і `patch`) будуть завантажені в пам'ять, так що переконайтеся, що параметр memorylimit налаштовано коректно.

### Дивіться також

-   [xdiffstringpatchbinary()](function.xdiff-string-patch-binary.html) - Псевдонім для xdiffstringbpatch