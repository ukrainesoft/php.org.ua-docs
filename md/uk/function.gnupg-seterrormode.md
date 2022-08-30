Встановлює режим звітування про помилки (errorreporting)

-   [« gnupgsetarmor](function.gnupg-setarmor.html)
    
-   [gnupgsetsignmode »](function.gnupg-setsignmode.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функції](ref.gnupg.html)
    
-   Встановлює режим звітування про помилки (errorreporting)
    

# gnupgseterrormode

(PECL gnupg >= 0.6)

gnupgseterrormode — Встановлює режим звітування про помилки (errorreporting)

### Опис

```methodsynopsis
gnupg_seterrormode(resource $identifier, int $errormode): void
```

Встановлює режим [errorreporting](errorfunc.configuration.html#ini.error-reporting)

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

`errormode`

Режим помилок.

`errormode` містить константу, що вказує, який тип errorreporting має бути використаний. Можливі значення: **`GNUPG_ERROR_WARNING`** **`GNUPG_ERROR_EXCEPTION`** і **`GNUPG_ERROR_SILENT`**. За замовчуванням використовується **`GNUPG_ERROR_SILENT`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **gnupgseterrormode()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
gnupg_seterrormode($res, GNUPG_ERROR_WARNING); // выводить PHP-предупреждения в случае возникновения ошибки
?>
```

**Приклад #2 Приклад використання **gnupgseterrormode()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$gpg->seterrormode(gnupg::ERROR_EXCEPTION); // исключение в случае возникновения ошибки
?>
```