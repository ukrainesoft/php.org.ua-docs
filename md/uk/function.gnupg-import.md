Імпортує ключ

-   [« gnupggettrustlist](function.gnupg-gettrustlist.html)
    
-   [gnupginit »](function.gnupg-init.html)
    
-   [PHP Manual](index.md)
    
-   [GnuPG Функції](ref.gnupg.md)
    
-   Імпортує ключ
    

# gnupgimport

(PECL gnupg >= 0.3)

gnupgimport — Імпорт ключа

### Опис

```methodsynopsis
gnupg_import(resource $identifier, string $keydata): array
```

Імпортує ключ `keydata` та повертає масив з інформацією про процес імпорту.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

`keydata`

Ключ імпорту.

### Значення, що повертаються

У разі успішного виконання повертає масив із інформацією про процес імпорту. У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gnupgimport()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
$info = gnupg_import($res,$keydata);
print_r($info);
?>
```

**Приклад #2 Приклад використання **gnupgimport()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$info = $gpg->import($keydata);
print_r($info);
?>
```