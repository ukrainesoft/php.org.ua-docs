---
navigation:
  - function.gnupg-encryptsign.md: « gnupgencryptsign
  - function.gnupg-getengineinfo.md: gnupggetengineinfo »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgexport
---
# gnupgexport

(PECL gnupg >= 0.1)

gnupgexport — Експортує ключ

### Опис

```methodsynopsis
gnupg_export(resource $identifier, string $fingerprint): string
```

Експортує ключ `fingerprint`

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

`fingerprint`

Відбиток ключа.

### Значення, що повертаються

У разі успішного виконання, функція повертає ключ. У разі помилки функція повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gnupgexport()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
$export = gnupg_export($res, "8660281B6051D071D94B5B230549F9DC851566DC");
echo $export;
?>
```

**Приклад #2 Приклад використання **gnupgexport()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$export = $gpg->export("8660281B6051D071D94B5B230549F9DC851566DC");
?>
```
