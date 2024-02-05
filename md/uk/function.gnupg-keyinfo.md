---
navigation:
  - function.gnupg-init.md: « gnupg\_init
  - function.gnupg-listsignatures.md: gnupg\_listsignatures »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_keyinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_keyinfo

(PECL gnupg >= 0.1)

gnupg\_keyinfo — Повертає масив з інформацією про всі ключі, які відповідають заданому шаблону

### Опис

```methodsynopsis
gnupg_keyinfo(resource $identifier, string $pattern): array|false
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`pattern`

Шаблон, що перевіряється на відповідність.

### Значення, що повертаються

Повертає масив з інформацією про всі ключі, які відповідають заданому шаблону або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**gnupg\_keyinfo()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
$info = gnupg_keyinfo($res, 'test');
print_r($info);
?>
```

**Пример #2 Пример использования**gnupg\_keyinfo()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$info = $gpg->keyinfo("test");
print_r($info);
?>
```
