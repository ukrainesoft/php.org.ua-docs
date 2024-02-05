---
navigation:
  - function.gnupg-encryptsign.md: « gnupg\_encryptsign
  - function.gnupg-getengineinfo.md: gnupg\_getengineinfo »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_export

(PECL gnupg >= 0.1)

gnupg\_export — Експортує ключ

### Опис

```methodsynopsis
gnupg_export(resource $identifier, string $fingerprint): string|false
```

Експортує ключ `fingerprint`

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`fingerprint`

Відбиток ключа.

### Значення, що повертаються

У разі успішного виконання, функція повертає ключ. У разі помилки функція повертає **`false`**

### Приклади

**Пример #1 Пример использования**gnupg\_export()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
$export = gnupg_export($res, "8660281B6051D071D94B5B230549F9DC851566DC");
echo $export;
?>
```

**Пример #2 Пример использования**gnupg\_export()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$export = $gpg->export("8660281B6051D071D94B5B230549F9DC851566DC");
?>
```
