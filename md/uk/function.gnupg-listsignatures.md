Перераховує підписи ключа

-   [« gnupg\_keyinfo](function.gnupg-keyinfo.html)
    
-   [gnupg\_setarmor »](function.gnupg-setarmor.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функции](ref.gnupg.html)
    
-   Перераховує підписи ключа
    

# gnupglistsignatures

(PECL gnupg >= 0.5)

gnupglistsignatures — Перелік підпису ключа

### Опис

```methodsynopsis
gnupg_listsignatures(resource $identifier, string $keyid): array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.html) або **gnupg**

`keyid`

Ідентифікатор ключа для списку підписів.

### Значення, що повертаються

У разі успішного виконання, функція повертає масив підписів ключів. У разі помилки функція повертає **`null`**

### Приклади

**Приклад #1 Приклад використання **gnupglistsignatures()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
$signatures = gnupg_listsignatures($res, "8660281B6051D071D94B5B230549F9DC851566DC");
print_r($signatures);
?>
```

**Приклад #2 Приклад використання **gnupglistsignatures()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$signatures = $gpg->listsignatures("8660281B6051D071D94B5B230549F9DC851566DC");
print_r($signatures);
?>
```