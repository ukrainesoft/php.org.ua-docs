---
navigation:
  - function.gnupg-getengineinfo.md: « gnupg\_getengineinfo
  - function.gnupg-geterrorinfo.md: gnupg\_geterrorinfo »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_geterror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_geterror

(PECL gnupg >= 0.1)

gnupg\_geterror — Повернення тексту повідомлення про помилку, якщо функція не була виконана

### Опис

```methodsynopsis
gnupg_geterror(resource $identifier): string|false
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

### Значення, що повертаються

Повертає текст повідомлення про помилку, якщо сталася помилка, інакше повертає **`false`**

### Приклади

**Пример #1 Пример использования**gnupg\_geterror()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
echo gnupg_geterror($res);
?>
```

**Пример #2 Пример использования**gnupg\_geterror()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
echo $gpg->geterror();
?>
```
