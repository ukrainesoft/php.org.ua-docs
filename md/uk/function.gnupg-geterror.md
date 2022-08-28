Повертає текст повідомлення про помилку, якщо функція не була виконана

-   [« gnupg\_getengineinfo](function.gnupg-getengineinfo.html)
    
-   [gnupg\_geterrorinfo »](function.gnupg-geterrorinfo.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функции](ref.gnupg.html)
    
-   Повертає текст повідомлення про помилку, якщо функція не була виконана
    

# gnupggeterror

(PECL gnupg >= 0.1)

gnupggeterror — Повертає текст повідомлення про помилку, якщо функція не була виконана

### Опис

```methodsynopsis
gnupg_geterror(resource $identifier): string
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.html) або **gnupg**

### Значення, що повертаються

Повертає текст повідомлення про помилку, якщо сталася помилка, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gnupggeterror()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
echo gnupg_geterror($res);
?>
```

**Приклад #2 Приклад використання **gnupggeterror()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
echo $gpg->geterror();
?>
```