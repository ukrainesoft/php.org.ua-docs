---
navigation:
  - function.xdiff-file-bdiff.html: xdifffilebdiff
  - function.xdiff-file-diff-binary.html: xdifffilediffbinary »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdifffilebpatch
---
# xdifffilebpatch

(PECL xdiff >= 1.5.0)

xdifffilebpatch — Застосувати бінарний патч до файлу

### Опис

```methodsynopsis
xdiff_file_bpatch(string $file, string $patch, string $dest): bool
```

Застосувати до файлу `file` патч `patch` і записати результат у файл `dest`. Ця функція приймає патчі, створені як [xdifffilebdiff()](function.xdiff-file-bdiff.html) так і [xdifffilerabdiff()](function.xdiff-file-rabdiff.md) або їх копії.

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

**Приклад #1 Приклад використання **xdifffilebpatch()****

У наступному коді показано застосування бінарного патчу до файлу.

```php
<?php
$old_version = 'archive-1.0.tgz';
$patch = 'archive.bpatch';

$result = xdiff_file_bpatch($old_version, $patch, 'archive-1.1.tgz');
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

-   [xdifffilebdiff()](function.xdiff-file-bdiff.md) - Створити бінарний патч порівнюючи два файли
-   [xdifffilerabdiff()](function.xdiff-file-rabdiff.md) - Створити бінарний патч порівнюючи два файли за допомогою поліномінального алгоритму Rabin fingerprinting
