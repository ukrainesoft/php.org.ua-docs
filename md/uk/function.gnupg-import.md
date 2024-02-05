---
navigation:
  - function.gnupg-gettrustlist.md: « gnupg\_gettrustlist
  - function.gnupg-init.md: gnupg\_init »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_import
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_import

(PECL gnupg >= 0.3)

gnupg\_import — Імпорт ключа

### Опис

```methodsynopsis
gnupg_import(resource $identifier, string $keydata): array|false
```

Імпортує ключ `keydata` та повертає масив з інформацією про процес імпорту.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`keydata`

Ключ імпорту.

### Значення, що повертаються

У разі успішного виконання повертає масив із інформацією про процес імпорту. У разі виникнення помилки повертає **`false`**

### Приклади

**Пример #1 Пример использования**gnupg\_import()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
$info = gnupg_import($res,$keydata);
print_r($info);
?>
```

**Пример #2 Пример использования**gnupg\_import()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$info = $gpg->import($keydata);
print_r($info);
?>
```
