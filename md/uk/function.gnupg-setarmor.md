Перемикає висновок у текстовому чи бінарному режимі

-   [« gnupg\_listsignatures](function.gnupg-listsignatures.html)
    
-   [gnupg\_seterrormode »](function.gnupg-seterrormode.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функции](ref.gnupg.html)
    
-   Перемикає висновок у текстовому чи бінарному режимі
    

# gnupgsetarmor

(PECL gnupg >= 0.1)

gnupgsetarmor — Переключає виведення текстового або бінарного режиму.

### Опис

```methodsynopsis
gnupg_setarmor(resource $identifier, int $armor): bool
```

Перемикає висновок у текстовому або бінарному режимі.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.html) або **gnupg**

`armor`

У разі ненульового цілого числа, функція включає текстовий режим виводу (за умовчанням). У разі 0 виведення в бінарному режимі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gnupgsetarmor()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
gnupg_setarmor($res,1); // текстовый режим вывода;
gnupg_setarmor($res,0); // бинарный режим вывода;
?>
```

**Приклад #2 Приклад використання **gnupgsetarmor()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$gpg->setarmor(1); // текстовый режим вывода;
$gpg->setarmor(0); // бинарный режим вывода;
?>
```