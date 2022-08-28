Видаляє всі ключі, які були встановлені для підписання раніше

-   [« gnupg\_clearencryptkeys](function.gnupg-clearencryptkeys.html)
    
-   [gnupg\_decrypt »](function.gnupg-decrypt.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функции](ref.gnupg.html)
    
-   Видаляє всі ключі, які були встановлені для підписання раніше
    

# gnupgclearsignkeys

(PECL gnupg >= 0.5)

gnupgclearsignkeys — Видалення всіх ключів, які були встановлені для підписання раніше

### Опис

```methodsynopsis
gnupg_clearsignkeys(resource $identifier): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.html) або **gnupg**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupgclearsignkeys()****

```php
<?php
$res = gnupg_init();
gnupg_clearsignkeys($res);
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupgclearsignkeys()****

```php
<?php
$gpg = new gnupg();
$gpg->clearsignkeys();
?>
```