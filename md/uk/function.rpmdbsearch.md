---
navigation:
  - function.rpmdbinfo.md: « rpmdbinfo
  - function.rpmgetsymlink.md: rpmgetsymlink »
  - index.md: PHP Manual
  - ref.rpminfo.md: Функції RpmInfo
title: rpmdbsearch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rpmdbsearch

(PECL rpminfo >= 0.3.0)

rpmdbsearch — Пошук RPM-пакетів

### Опис

```methodsynopsis
rpmdbsearch(    string $pattern,    int $rpmtag = RPMTAG_NAME,    int $rpmmire = -1,    bool $full = false): ?array
```

Пошук пакетів у системній базі даних RPM.

### Список параметрів

`pattern`

Значення, яке шукатимемо.

`rpmtag`

Критерій пошуку. Одна з констант RPMTAG\_\*, смотрите[константи rpminfo](rpminfo.constants.md)

`rpmmire`

Тип шаблону. Одна з констант RPMMIRE\_\*, смотрите[константи rpminfo](rpminfo.constants.md). Якщо менше 0, то критерій повинен дорівнювати значенню і по можливості буде використаний індекс бази даних.

`full`

Якщо **`true`**, для файлу будуть вилучені всі заголовки. Інакше буде вилучено мінімальний набір.

### Значення, що повертаються

Масив масивів з інформацією, або **`null`**, у разі виникнення помилки.

### Приклади

**Приклад #1 Пошук пакета, в якому знаходиться файл**

```php
<?php
$info = rpmdbsearch("/usr/bin/php", RPMTAG_INSTFILENAMES);
print_r($info);
?>
```

Результат виконання наведеного прикладу:

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

-   [rpmaddtag()](function.rpmaddtag.md) \- Додає тег, отриманий у запиті
