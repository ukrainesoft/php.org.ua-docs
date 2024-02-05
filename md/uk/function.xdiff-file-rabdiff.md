---
navigation:
  - function.xdiff-file-patch.md: « xdiff\_file\_patch
  - function.xdiff-string-bdiff-size.md: xdiff\_string\_bdiff\_size »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_file\_rabdiff
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_file\_rabdiff

(PECL xdiff >= 1.5.0)

xdiff\_file\_rabdiff — Створити бінарний патч порівнюючи два файли за допомогою поліномінального алгоритму Rabin fingerprinting

### Опис

```methodsynopsis
xdiff_file_rabdiff(string $old_file, string $new_file, string $dest): bool
```

Створює бінарний патч, порівнюючи два файли і зберігає результат у файл. Ця функція відрізняється від [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.md) використовуваним алгоритмом, який працює швидше та виробляє патчі меншого розміру. Ця функція працює як з текстом, так і з бінарними даними. Патч згодом можна застосувати за допомогою функцій [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md) [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md)

Детальніше різниця алгоритмів пояснена на сайті [» libxdiff](http://www.xmailserver.org/xdiff-lib.md)

### Список параметрів

`old_file`

Шлях до першого, "старого" файлу.

`new_file`

Шлях до другого, "нового" файлу.

`dest`

Шлях результуючого файлу патчу. Він міститиме різницю між старим і новим файлом у бінарному, человеконечитаемом форматі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** xdiff\_file\_rabdiff()\*\*\*\*

Наступний код порівнює два архіви та створює патч.

```php
<?php
$old_version = 'my_script_1.0.tgz';
$new_version = 'my_script_1.1.tgz';

xdiff_file_rabdiff($old_version, $new_version, 'my_script.bdiff');
?>
```

### Примітки

> **Зауваження** :
> 
> Обидва файли будуть завантажені в пам'ять, тому переконайтеся, що параметр memory\_limit налаштовано коректно.

### Дивіться також

-   [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md) \- Застосувати бінарний патч до файлу
