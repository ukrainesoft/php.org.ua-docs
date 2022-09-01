---
navigation:
  - function.xdiff-file-bpatch.html: xdifffilebpatch
  - function.xdiff-file-diff.html: xdifffilediff »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdifffilediffbinary
---
# xdifffilediffbinary

(PECL xdiff >= 0.2.0)

xdifffilediffbinary - Псевдонім для xdifffilebdiff

### Опис

```methodsynopsis
xdiff_file_diff_binary(string $old_file, string $new_file, string $dest): bool
```

Створює файл бінарного патчу, порівнюючи два файли. Ця функція працює як з бінарними, так і текстовими файлами. Надалі отриманий патч можна застосувати за допомогою функцій [xdifffilebpatch()](function.xdiff-file-bpatch.html)

Починаючи з версії 1.5.0, ця функція є псевдонімом [xdifffilebdiff()](function.xdiff-file-bdiff.html)

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

-   [xdifffilebdiff()](function.xdiff-file-bdiff.html) - Створити бінарний патч порівнюючи два файли
-   [xdifffilebpatch()](function.xdiff-file-bpatch.html) - Застосувати бінарний патч до файлу
