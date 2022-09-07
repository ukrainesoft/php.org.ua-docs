---
navigation:
  - function.xdiff-file-bdiff-size.md: xdifffilebdiffsize
  - function.xdiff-file-bpatch.md: xdifffilebpatch »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdifffilebdiff
---
# xdifffilebdiff

(PECL xdiff >= 1.5.0)

xdifffilebdiff — Створити бінарний патч порівнюючи два файли

### Опис

```methodsynopsis
xdiff_file_bdiff(string $old_file, string $new_file, string $dest): bool
```

Створює файл бінарного патчу, порівнюючи два файли. Ця функція працює як з бінарними, так і текстовими файлами. Надалі отриманий патч можна застосувати за допомогою функцій [xdifffilebpatch()](function.xdiff-file-bpatch.md)[xdiffstringbpatch()](function.xdiff-string-bpatch.md)

### Список параметрів

`old_file`

Шлях до першого, "старого" файлу.

`new_file`

Шлях до другого, "нового" файлу.

`dest`

Шлях результуючого файлу патчу. Він міститиме різницю між старим і новим файлом у бінарному, человеконечитаемом форматі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **xdifffilebdiff()****

Наступний код створює бінарний патч.

```php
<?php
$old_version = 'my_script_1.0.tgz';
$new_version = 'my_script_1.1.tgz';

xdiff_file_bdiff($old_version, $new_version, 'my_script.bdiff');
?>
```

### Примітки

> **Зауваження**
> 
> Обидва файли будуть завантажені в пам'ять, тому переконайтеся, що параметр memorylimit налаштовано коректно.

### Дивіться також

-   [xdifffilebpatch()](function.xdiff-file-bpatch.md) - Застосувати бінарний патч до файлу
