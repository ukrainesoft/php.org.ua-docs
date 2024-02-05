---
navigation:
  - function.gnupg-keyinfo.md: « gnupg\_keyinfo
  - function.gnupg-setarmor.md: gnupg\_setarmor »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_listsignatures
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_listsignatures

(PECL gnupg >= 0.5)

gnupg\_listsignatures — Перелік підпису ключа

### Опис

```methodsynopsis
gnupg_listsignatures(resource $identifier, string $keyid): ?array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`keyid`

Ідентифікатор ключа для списку підписів.

### Значення, що повертаються

У разі успішного виконання, функція повертає масив підписів ключів. У разі помилки функція повертає **`null`**

### Приклади

**Пример #1 Пример использования**gnupg\_listsignatures()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
$signatures = gnupg_listsignatures($res, "8660281B6051D071D94B5B230549F9DC851566DC");
print_r($signatures);
?>
```

**Пример #2 Пример использования**gnupg\_listsignatures()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$signatures = $gpg->listsignatures("8660281B6051D071D94B5B230549F9DC851566DC");
print_r($signatures);
?>
```
