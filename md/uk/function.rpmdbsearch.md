Пошук RPM-пакетів

-   [« rpmdbinfo](function.rpmdbinfo.html)
    
-   [rpminfo »](function.rpminfo.html)
    
-   [PHP Manual](index.html)
    
-   [Функції RpmInfo](ref.rpminfo.html)
    
-   Пошук RPM-пакетів
    

# rpmdbsearch

(PECL rpminfo >= 0.3.0)

rpmdbsearch — Пошук RPM-пакетів

### Опис

```methodsynopsis
rpmdbsearch(    string $pattern,    int $rpmtag = RPMTAG_NAME,    int $rpmmire = -1,    bool $full = false): array
```

Пошук пакетів у системній базі даних RPM.

### Список параметрів

`pattern`

Значення, яке шукатимемо.

`rpmtag`

Критерій пошуку. Одна з констант RPMTAG, дивіться [константы rpminfo](rpminfo.constants.html)

`rpmmire`

Тип шаблону. Одна з констант RPMMIRE, дивіться [константы rpminfo](rpminfo.constants.html). Якщо менше 0, то критерій повинен дорівнювати значенню і по можливості буде використаний індекс бази даних.

`full`

Якщо **`true`**, то для файлу буде вилучено всі заголовки. Інакше буде вилучено мінімальний набір.

### Значення, що повертаються

Масив масивів з інформацією, або **`null`**, у разі виникнення помилки.

### Приклади

**Приклад #1 Пошук пакета, в якому знаходиться файл**

```php
<?php
$info = rpmdbsearch("/usr/bin/php", RPMTAG_INSTFILENAMES);
print_r($info);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => Array
        (
            [Name] => php-cli
            [Version] => 7.4.4
            [Release] => 1.fc32
            [Summary] => Command-line interface for PHP
            [Arch] => x86_64
        )

)
```

### Дивіться також

-   [rpmaddtag()](function.rpmaddtag.html) - Додає тег, отриманий у запиті