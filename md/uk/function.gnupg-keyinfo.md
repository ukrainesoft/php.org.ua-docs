---
navigation:
  - function.gnupg-init.md: « gnupginit
  - function.gnupg-listsignatures.md: gnupglistsignatures »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgkeyinfo
---
# gnupgkeyinfo

(PECL gnupg >= 0.1)

gnupgkeyinfo — Повертає масив з інформацією про всі ключі, які відповідають заданому шаблону

### Опис

```methodsynopsis
gnupg_keyinfo(resource $identifier, string $pattern): array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

`pattern`

Шаблон, що перевіряється на відповідність.

### Значення, що повертаються

Повертає масив з інформацією про всі ключі, які відповідають заданому шаблону або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gnupgkeyinfo()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
$info = gnupg_keyinfo($res, 'test');
print_r($info);
?>
```

**Приклад #2 Приклад використання **gnupgkeyinfo()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$info = $gpg->keyinfo("test");
print_r($info);
?>
```
