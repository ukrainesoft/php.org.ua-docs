Додати ключ для підписання

-   [« gnupg\_addencryptkey](function.gnupg-addencryptkey.html)
    
-   [gnupg\_cleardecryptkeys »](function.gnupg-cleardecryptkeys.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функции](ref.gnupg.html)
    
-   Додати ключ для підписання
    

# gnupgaddsignkey

(PECL gnupg >= 0.5)

gnupgaddsignkey — Додати ключ для підписання

### Опис

```methodsynopsis
gnupg_addsignkey(resource $identifier, string $fingerprint, string $passphrase = ?): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.html) або **gnupg**

`fingerprint`

Відбиток ключа.

`passphrase`

Пароль.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupgaddsignkey()****

```php
<?php
$res = gnupg_init();
gnupg_addsignkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupgaddsignkey()****

```php
<?php
$gpg = new gnupg();
$gpg->addsignkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
?>
```