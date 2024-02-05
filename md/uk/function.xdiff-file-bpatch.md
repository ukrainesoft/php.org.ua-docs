---
navigation:
  - function.xdiff-file-bdiff.md: « xdiff\_file\_bdiff
  - function.xdiff-file-diff-binary.md: xdiff\_file\_diff\_binary »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_file\_bpatch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_file\_bpatch

(PECL xdiff >= 1.5.0)

xdiff\_file\_bpatch — Застосувати бінарний патч до файлу

### Опис

```methodsynopsis
xdiff_file_bpatch(string $file, string $patch, string $dest): bool
```

Применить к файлу`file`патч`patch`и записать результат в файл`dest`. Ця функція приймає патчі, створені як [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.md)так и[xdiff\_file\_rabdiff()](function.xdiff-file-rabdiff.md) або їх копії.

### Список параметрів

`file`

Оригінальний файл.

`patch`

Файл бінарний патч.

`dest`

Підсумковий файл.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** xdiff\_file\_bpatch()\*\*\*\*

У наступному коді показано застосування бінарного патчу до файлу.

```php
<?php
$old_version = 'archive-1.0.tgz';
$patch = 'archive.bpatch';

$result = xdiff_file_bpatch($old_version, $patch, 'archive-1.1.tgz');
if ($result) {
   echo "Файл пропатчен";
} else {
   echo "Файл не может быть пропатчен";
}

?>
```

### Примітки

> **Зауваження** :
> 
> Обидва файли (`file`и`patch`) будуть завантажені в пам'ять, так що переконайтеся, що параметр memory\_limit налаштовано коректно.

### Дивіться також

-   [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.md) \- Створити бінарний патч порівнюючи два файли
-   [xdiff\_file\_rabdiff()](function.xdiff-file-rabdiff.md) \- Створити бінарний патч порівнюючи два файли за допомогою поліномінального алгоритму Rabin fingerprinting
