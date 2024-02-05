---
navigation:
  - function.xdiff-file-merge3.md: « xdiff\_file\_merge3
  - function.xdiff-file-patch.md: xdiff\_file\_patch »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_file\_patch\_binary
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_file\_patch\_binary

(PECL xdiff >= 0.2.0)

xdiff\_file\_patch\_binary — Псевдоним[xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md)

### Опис

```methodsynopsis
xdiff_file_patch_binary(string $file, string $patch, string $dest): bool
```

Применить к файлу`file`патч`patch`и записать результат в файл`dest`. Ця функція приймає патчі створені як [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.md)так и[xdiff\_file\_rabdiff()](function.xdiff-file-rabdiff.md) або їх копії.

Починаючи з версії 1.5.0, ця функція є псевдонімом [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md)

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

**Приклад #1 Приклад використання** xdiff\_file\_patch\_binary()\*\*\*\*

У наступному коді показано застосування бінарного патчу до файлу.

```php
<?php
$old_version = 'archive-1.0.tgz';
$patch = 'archive.bpatch';

$result = xdiff_file_patch_binary($old_version, $patch, 'archive-1.1.tgz');
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

-   [xdiff\_string\_patch\_binary()](function.xdiff-string-patch-binary.md) \- Псевдонім xdiff\_string\_bpatch
