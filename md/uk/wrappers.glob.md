---
navigation:
  - wrappers.data.md: '« data://'
  - wrappers.phar.md: 'phar:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'glob://'
---
# glob://

glob:// — Знаходження шляхів, що відповідають шаблону

### Опис

Обгортка потоку glob:.

### Використання

-   glob://

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allowurlfopen](filesystem.configuration.html#ini.allow-url-fopen) | Ні |
| Обмеження по [allowurlinclude](filesystem.configuration.html#ini.allow-url-include) | Ні |
| Читання | Ні |
| Запис | Ні |
| Додавання | Ні |
| Одночасне читання та запис | Ні |
| Підтримка [stat()](function.stat.md) | Ні |
| Підтримка [unlink()](function.unlink.md) | Ні |
| Підтримка [rename()](function.rename.md) | Ні |
| Підтримка [mkdir()](function.mkdir.md) | Ні |
| Підтримка [rmdir()](function.rmdir.md) | Ні |

### Приклади

**Приклад #1 Основи використання**

```php
<?php
// Просмотреть все файлы *.php в директории ext/spl/examples/
// и напечатать имена файлов и их размеры
$it = new DirectoryIterator("glob://ext/spl/examples/*.php");
foreach($it as $f) {
    printf("%s: %.1FK\n", $f->getFilename(), $f->getSize()/1024);
}
?>
```

```
tree.php: 1.0K
findregex.php: 0.6K
findfile.php: 0.7K
dba_dump.php: 0.9K
nocvsdir.php: 1.1K
phar_from_dir.php: 1.0K
ini_groups.php: 0.9K
directorytree.php: 0.9K
dba_array.php: 1.1K
class_tree.php: 1.8K
```
