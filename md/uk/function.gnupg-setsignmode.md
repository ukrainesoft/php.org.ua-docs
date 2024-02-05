---
navigation:
  - function.gnupg-seterrormode.md: « gnupg\_seterrormode
  - function.gnupg-sign.md: gnupg\_sign »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_setsignmode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_setsignmode

(PECL gnupg >= 0.1)

gnupg\_setsignmode — Встановлює режим підписування

### Опис

```methodsynopsis
gnupg_setsignmode(resource $identifier, int $signmode): bool
```

Встановлює режим підписування.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`sigmode`

Режим підписування.

`signmode` містить константу, що вказує, який тип підпису має бути зроблено. Можливі значення: **`GNUPG_SIG_MODE_NORMAL`** **`GNUPG_SIG_MODE_DETACH`**и**`GNUPG_SIG_MODE_CLEAR`**По умолчанию используется**`GNUPG_SIG_MODE_CLEAR`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**gnupg\_setsignmode()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
gnupg_setsignmode($res, GNUPG_SIG_MODE_DETACH); // производить раздельную подпись
?>
```

**Пример #2 Пример использования**gnupg\_setsignmode()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$gpg->setsignmode(gnupg::SIG_MODE_DETACH); // производить раздельную подпись
?>
```
