Повертає поточний активний протокол для всіх операцій

-   [« gnupggeterrorinfo](function.gnupg-geterrorinfo.html)
    
-   [gnupggettrustlist »](function.gnupg-gettrustlist.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функції](ref.gnupg.html)
    
-   Повертає поточний активний протокол для всіх операцій
    

# gnupggetprotocol

(PECL gnupg >= 0.1)

gnupggetprotocol — Повертає поточний активний протокол для всіх операцій

### Опис

```methodsynopsis
gnupg_getprotocol(resource $identifier): int
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

### Значення, що повертаються

Повертає поточний активний протокол, який може бути одним із **`GNUPG_PROTOCOL_OpenPGP`** або **`GNUPG_PROTOCOL_CMS`**

### Приклади

**Приклад #1 Приклад використання **gnupggetprotocol()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
echo gnupg_getprotocol($res);
?>
```

**Приклад #2 Приклад використання **gnupggetprotocol()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
echo $gpg->getprotocol();
?>
```