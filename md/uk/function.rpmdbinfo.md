---
navigation:
  - function.rpmaddtag.md: « rpmaddtag
  - function.rpmdbsearch.md: rpmdbsearch »
  - index.md: PHP Manual
  - ref.rpminfo.md: Функції RpmInfo
title: rpmdbinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rpmdbinfo

(PECL rpminfo >= 0.2.0)

rpmdbinfo — Отримує інформацію від встановленого RPM

### Опис

```methodsynopsis
rpmdbinfo(string $nevr, bool $full = false): ?array
```

Отримує інформацію про встановлений пакет із системної бази даних RPM.

### Список параметрів

`nevr`

Ім'я із зазначенням епохи, версії та випуску.

`full`

Якщо **`true`**, Виймаються всі інформаційні заголовки для файлу, інакше тільки мінімальний набір.

### Значення, що повертаються

Масив (array) масивів (array) інформації або NULL у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** rpmdbinfo()\*\*\*\*

```php
<?php
rpmaddtag(RPMTAG_INSTALLTIME);
$info = rpmdbinfo("php-pecl-rpminfo");
print_r($info);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Array
        (
            [Name] => php-pecl-rpminfo
            [Version] => 0.4.2
            [Release] => 1.fc31
            [Summary] => RPM information
            [Installtime] => 1586244687
            [Arch] => x86_64
        )
)
```

### Дивіться також

-   [rpmaddtag()](function.rpmaddtag.md) \- Додає тег, отриманий у запиті
