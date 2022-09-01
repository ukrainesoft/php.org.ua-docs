---
navigation:
  - function.gnupg-seterrormode.html: « gnupgseterrormode
  - function.gnupg-sign.html: gnupgsign »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgsetsignmode
---
# gnupgsetsignmode

(PECL gnupg >= 0.1)

gnupgsetsignmode — Встановлює режим підписування

### Опис

```methodsynopsis
gnupg_setsignmode(resource $identifier, int $signmode): bool
```

Встановлює режим підписування.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

`sigmode`

Режим підписування.

`signmode` містить константу, що вказує, який тип підпису має бути зроблено. Можливі значення: **`GNUPG_SIG_MODE_NORMAL`** **`GNUPG_SIG_MODE_DETACH`** і **`GNUPG_SIG_MODE_CLEAR`**. За замовчуванням використовується **`GNUPG_SIG_MODE_CLEAR`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gnupgsetsignmode()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
gnupg_setsignmode($res, GNUPG_SIG_MODE_DETACH); // производить раздельную подпись
?>
```

**Приклад #2 Приклад використання **gnupgsetsignmode()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$gpg->setsignmode(gnupg::SIG_MODE_DETACH); // производить раздельную подпись
?>
```
