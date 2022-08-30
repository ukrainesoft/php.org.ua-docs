Відкриває файл, стислий за допомогою bzip2

-   [« bzflush](function.bzflush.html)
    
-   [bzread »](function.bzread.html)
    
-   [PHP Manual](index.html)
    
-   [Функції Bzip2](ref.bzip2.html)
    
-   Відкриває файл, стислий за допомогою bzip2
    

# bzopen

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

bzopen — Відкриває файл, стислий за допомогою bzip2

### Опис

```methodsynopsis
bzopen(string|resource $file, string $mode): resource|false
```

**bzopen()** відкриває bzip2 (.bz2) файл читання чи записи.

### Список параметрів

`file`

Ім'я файлу, що відкривається, або існуючий ресурс потоку.

`mode`

Підтримуються лише `'r'` (читання) та `'w'` (Запис). Все інше змусить **bzopen()** повернути **`false`**

### Значення, що повертаються

**bzopen()** повертається покажчик на відкритий файл, або **`false`**, якщо відкрити файл не вдалося.

### Приклади

**Приклад #1 Приклад використання **bzopen()****

```php
<?php

$file = "/tmp/foo.bz2";
$bz = bzopen($file, "r") or die("Не могу открыть $file для чтения");

bzclose($bz);

?>
```

### Дивіться також

-   [bzclose()](function.bzclose.html) - Закриває файл bzip2