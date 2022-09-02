---
navigation:
  - ref.gnupg.md: « GnuPG Функції
  - function.gnupg-addencryptkey.md: gnupgaddencryptkey »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgadddecryptkey
---
# gnupgadddecryptkey

(PECL gnupg >= 0.5)

gnupgadddecryptkey — Додати ключ для розшифровки

### Опис

```methodsynopsis
gnupg_adddecryptkey(resource $identifier, string $fingerprint, string $passphrase): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

`fingerprint`

Відбиток ключа.

`passphrase`

Кодове слово.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gnupgadddecryptkey()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
gnupg_adddecryptkey($res,"8660281B6051D071D94B5B230549F9DC851566DC","test");
?>
```

**Приклад #2 Приклад використання **gnupgadddecryptkey()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$gpg->adddecryptkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
?>
```
