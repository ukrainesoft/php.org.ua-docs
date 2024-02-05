---
navigation:
  - ref.gnupg.md: « GnuPG Функції
  - function.gnupg-addencryptkey.md: gnupg\_addencryptkey »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_adddecryptkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_adddecryptkey

(PECL gnupg >= 0.5)

gnupg\_adddecryptkey — Додати ключ для розшифровки

### Опис

```methodsynopsis
gnupg_adddecryptkey(resource $identifier, string $fingerprint, string $passphrase): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`fingerprint`

Відбиток ключа.

`passphrase`

Кодове слово.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**gnupg\_adddecryptkey()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
gnupg_adddecryptkey($res,"8660281B6051D071D94B5B230549F9DC851566DC","test");
?>
```

**Пример #2 Пример использования**gnupg\_adddecryptkey()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$gpg->adddecryptkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
?>
```
