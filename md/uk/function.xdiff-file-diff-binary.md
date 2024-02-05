---
navigation:
  - function.xdiff-file-bpatch.md: « xdiff\_file\_bpatch
  - function.xdiff-file-diff.md: xdiff\_file\_diff »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_file\_diff\_binary
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_file\_diff\_binary

(PECL xdiff >= 0.2.0)

xdiff\_file\_diff\_binary — Псевдоним[xdiff\_file\_bdiff()](function.xdiff-file-bdiff.md)

### Опис

```methodsynopsis
xdiff_file_diff_binary(string $old_file, string $new_file, string $dest): bool
```

Створює файл бінарного патчу, порівнюючи два файли. Ця функція працює як з бінарними, так і текстовими файлами. Надалі отриманий патч можна застосувати за допомогою функцій [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md)

Починаючи з версії 1.5.0, ця функція є псевдонімом [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.md)

### Список параметрів

`old_file`

Шлях до першого, "старого" файлу.

`new_file`

Шлях до другого, "нового" файлу.

`dest`

Шлях результуючого файлу патчу. Він міститиме різницю між старим і новим файлом у бінарному, людинонечитаемом.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Апмсер использования**xdiff\_file\_diff\_binary()\*\*\*\*

Наступний код створює бінарний патч, порівнюючи два архіви.

```php
<?php
$old_version = 'my_script_1.0.tgz';
$new_version = 'my_script_1.1.tgz';

xdiff_file_diff_binary($old_version, $new_version, 'my_script.bdiff');
?>
```

### Примітки

> **Зауваження** :
> 
> Обидва файли будуть завантажені в пам'ять, тому переконайтеся, що параметр memory\_limit налаштовано коректно.

### Дивіться також

-   [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.md) \- Створити бінарний патч порівнюючи два файли
-   [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md) \- Застосувати бінарний патч до файлу
