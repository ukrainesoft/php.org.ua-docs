---
navigation:
  - function.gnupg-setarmor.md: « gnupg\_setarmor
  - function.gnupg-setsignmode.md: gnupg\_setsignmode »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_seterrormode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_seterrormode

(PECL gnupg >= 0.6)

gnupg\_seterrormode — Встановлює режим звітування про помилки (error\_reporting)

### Опис

```methodsynopsis
gnupg_seterrormode(resource $identifier, int $errormode): void
```

Устанавливает режим[error\_reporting](errorfunc.configuration.md#ini.error-reporting)

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`errormode`

Режим помилок.

`errormode` містить константу, що вказує, який тип error\_reporting має бути використаний. Можливі значення: **`GNUPG_ERROR_WARNING`** **`GNUPG_ERROR_EXCEPTION`**и**`GNUPG_ERROR_SILENT`**По умолчанию используется**`GNUPG_ERROR_SILENT`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**gnupg\_seterrormode()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
gnupg_seterrormode($res, GNUPG_ERROR_WARNING); // выводить PHP-предупреждения в случае возникновения ошибки
?>
```

**Пример #2 Пример использования**gnupg\_seterrormode()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$gpg->seterrormode(gnupg::ERROR_EXCEPTION); // исключение в случае возникновения ошибки
?>
```
