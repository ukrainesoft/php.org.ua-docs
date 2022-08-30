Підписує переданий текст

-   [« gnupgsetsignmode](function.gnupg-setsignmode.html)
    
-   [gnupgverify »](function.gnupg-verify.html)
    
-   [PHP Manual](index.md)
    
-   [GnuPG Функції](ref.gnupg.md)
    
-   Підписує переданий текст
    

# gnupgsign

(PECL gnupg >= 0.1)

gnupgsign — Підписує переданий текст

### Опис

```methodsynopsis
gnupg_sign(resource $identifier, string $plaintext): string
```

Підписує переданий у параметрі `plaintext` текст ключем, який був раніше встановлений за допомогою [gnupgaddsignkey](function.gnupg-addsignkey.html) і повертає підписаний текст або підпис, залежно від того, що було встановлено [gnupgsetsignmode](function.gnupg-setsignmode.html)

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

`plaintext`

Простий текст для підписання.

### Значення, що повертаються

У разі успішного виконання, функція повертає підписаний текст або підпис. У разі помилки функція повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gnupgsign()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
gnupg_addsignkey($res,"8660281B6051D071D94B5B230549F9DC851566DC","test");
$signed = gnupg_sign($res, "просто тест");
echo $signed;
?>
```

**Приклад #2 Приклад використання **gnupgsign()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$gpg->addsignkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
$signed = $gpg->sign("просто тест");
echo $signed;
?>
```