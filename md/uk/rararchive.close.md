Закриває RAR архів та звільняє всі ресурси

-   [« RarArchive](class.rararchive.html)
    
-   [RarArchive::getComment »](rararchive.getcomment.html)
    
-   [PHP Manual](index.html)
    
-   [RarArchive](class.rararchive.html)
    
-   Закриває RAR архів та звільняє всі ресурси
    

# RarArchive::close

# rarclose

(PECL rar >= 2.0.0)

RarArchive::close -- rarclose — Закриває RAR архів та звільняє всі ресурси

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public RarArchive::close(): bool
```

Процедурний стиль:

```methodsynopsis
rar_close(RarArchive $rarfile): bool
```

Закриває RAR архів та звільняє всі ресурси, пов'язані з ним.

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.html), відкритий за допомогою [rar\_open()](rararchive.open.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL rar 2.0.0 | Елементи архіву, що повертаються [RarArchive::getEntry()](rararchive.getentry.html) і [RarArchive::getEntries()](rararchive.getentries.html) тепер недійсні після виклику цього методу. Це означає, що немає гарантії правильної роботи всіх методів цих елементів. |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$rar_arch = RarArchive::open('latest_winrar.rar');
echo $rar_arch."\n";
$rar_arch->close();
echo $rar_arch."\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar"
RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar" (closed)
```

**Приклад #2 Процедурний стиль**

```php
<?php
$rar_arch = rar_open('latest_winrar.rar');
echo $rar_arch."\n";
rar_close($rar_arch);
echo $rar_arch."\n";
?>
```