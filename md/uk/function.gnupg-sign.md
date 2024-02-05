---
navigation:
  - function.gnupg-setsignmode.md: « gnupg\_setsignmode
  - function.gnupg-verify.md: gnupg\_verify »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_sign
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_sign

(PECL gnupg >= 0.1)

gnupg\_sign — Підписує переданий текст

### Опис

```methodsynopsis
gnupg_sign(resource $identifier, string $plaintext): string|false
```

Підписує переданий у параметрі `plaintext` текст ключем, який був раніше встановлений за допомогою [gnupg\_addsignkey](function.gnupg-addsignkey.md) і повертає підписаний текст або підпис, залежно від того, що було встановлено [gnupg\_setsignmode](function.gnupg-setsignmode.md)

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`plaintext`

Простий текст для підписання.

### Значення, що повертаються

У разі успішного виконання, функція повертає підписаний текст або підпис. У разі помилки функція повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** gnupg\_sign()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
gnupg_addsignkey($res,"8660281B6051D071D94B5B230549F9DC851566DC","test");
$signed = gnupg_sign($res, "просто тест");
echo $signed;
?>
```

**Приклад #2 Приклад використання** gnupg\_sign()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$gpg->addsignkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
$signed = $gpg->sign("просто тест");
echo $signed;
?>
```
