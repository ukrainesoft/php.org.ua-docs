Вийняти інформацію з RPM-файлу

-   [« rpmdbsearch](function.rpmdbsearch.html)
    
-   [rpmvercmp »](function.rpmvercmp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции RpmInfo](ref.rpminfo.html)
    
-   Вийняти інформацію з RPM-файлу
    

# rpminfo

(PECL rpminfo >= 0.1.0)

rpminfo — Витягти інформацію з RPM-файлу

### Опис

```methodsynopsis
rpminfo(string $path, bool $full = false, string &$error = ?): array
```

Вийняти інформацію про локальний файл RPM.

### Список параметрів

`path`

Шлях до файлу.

`full`

Якщо **`true`**, то для файлу буде вилучено всі заголовки. Інакше буде вилучено мінімальний набір.

`error`

Якщо заданий, то нього буде записана інформація про помилку, у разі її виникнення. Це дозволить уникнути попереджень під час виконання.

### Значення, що повертаються

Масив з даними або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **rpminfo()****

```php
<?php
rpmaddtag(RPMTAG_BUILDTIME);
$info = rpminfo("./php-pecl-rpminfo-0.4.2-1.el8.remi.7.4.x86_64.rpm");
print_r($info);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [Name] => php-pecl-rpminfo
    [Version] => 0.4.2
    [Release] => 1.el8
    [Summary] => RPM information
    [Buildtime] => 1586244821
    [Arch] => x86_64
)
```

### Дивіться також

-   [rpmaddtag()](function.rpmaddtag.html) - Додає тег, отриманий у запиті