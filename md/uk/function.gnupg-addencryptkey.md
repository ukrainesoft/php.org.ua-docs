---
navigation:
  - function.gnupg-adddecryptkey.md: « gnupgadddecryptkey
  - function.gnupg-addsignkey.md: gnupgaddsignkey »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgaddencryptkey
---
# gnupgaddencryptkey

(PECL gnupg >= 0.5)

gnupgaddencryptkey — Додає ключ для шифрування

### Опис

```methodsynopsis
gnupg_addencryptkey(resource $identifier, string $fingerprint): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

`fingerprint`

Відбиток ключа.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupgaddencryptkey()****

```php
<?php
$res = gnupg_init();
gnupg_addencryptkey($res, "8660281B6051D071D94B5B230549F9DC851566DC");
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupgaddencryptkey()****

```php
<?php
$gpg = new gnupg();
$gpg->addencryptkey("8660281B6051D071D94B5B230549F9DC851566DC");
?>
```
