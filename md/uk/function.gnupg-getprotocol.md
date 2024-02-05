---
navigation:
  - function.gnupg-geterrorinfo.md: « gnupg\_geterrorinfo
  - function.gnupg-gettrustlist.md: gnupg\_gettrustlist »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_getprotocol
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_getprotocol

(PECL gnupg >= 0.1)

gnupg\_getprotocol — Повертає поточний активний протокол для всіх операцій

### Опис

```methodsynopsis
gnupg_getprotocol(resource $identifier): int
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

### Значення, що повертаються

Повертає поточний активний протокол, який може бути одним з **`GNUPG_PROTOCOL_OpenPGP`**или**`GNUPG_PROTOCOL_CMS`**

### Приклади

**Пример #1 Пример использования**gnupg\_getprotocol()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
echo gnupg_getprotocol($res);
?>
```

**Пример #2 Пример использования**gnupg\_getprotocol()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
echo $gpg->getprotocol();
?>
```
