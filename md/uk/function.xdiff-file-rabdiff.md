Створити бінарний патч порівнюючи два файли за допомогою поліномінального алгоритму Rabin fingerprinting

-   [« xdiff\_file\_patch](function.xdiff-file-patch.html)
    
-   [xdiff\_string\_bdiff\_size »](function.xdiff-string-bdiff-size.html)
    
-   [PHP Manual](index.html)
    
-   [Функции xdiff](ref.xdiff.html)
    
-   Створити бінарний патч порівнюючи два файли за допомогою поліномінального алгоритму Rabin fingerprinting
    

# xdifffilerabdiff

(PECL xdiff >= 1.5.0)

xdifffilerabdiff — Створити бінарний патч порівнюючи два файли за допомогою поліномінального алгоритму Rabin fingerprinting

### Опис

```methodsynopsis
xdiff_file_rabdiff(string $old_file, string $new_file, string $dest): bool
```

Створює бінарний патч, порівнюючи два файли і зберігає результат у файл. Ця функція відрізняється від [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.html) використовуваним алгоритмом, який працює швидше та виробляє патчі меншого розміру. Ця функція працює як з текстом, так і з бінарними даними. Патч згодом можна застосувати за допомогою функцій [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.html)[xdiff\_string\_bpatch()](function.xdiff-string-bpatch.html)

Детальніше різниця алгоритмів пояснена на сайті [» libxdiff](http://www.xmailserver.org/xdiff-lib.html)

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

**Приклад #1 Приклад використання **xdifffilerabdiff()****

Наступний код порівнює два архіви та створює патч.

```php
<?php
$old_version = 'my_script_1.0.tgz';
$new_version = 'my_script_1.1.tgz';

xdiff_file_rabdiff($old_version, $new_version, 'my_script.bdiff');
?>
```

### Примітки

> **Зауваження**
> 
> Обидва файли будуть завантажені в пам'ять, тому переконайтеся, що параметр memorylimit налаштовано коректно.

### Дивіться також

-   [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.html) - Застосувати бінарний патч до файлу