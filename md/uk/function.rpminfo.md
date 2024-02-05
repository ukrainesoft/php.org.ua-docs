---
navigation:
  - function.rpmgetsymlink.md: « rpmgetsymlink
  - function.rpmvercmp.md: rpmvercmp »
  - index.md: PHP Manual
  - ref.rpminfo.md: Функції RpmInfo
title: rpminfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rpminfo

(PECL rpminfo >= 0.1.0)

rpminfo — Витягти інформацію з RPM-файлу

### Опис

```methodsynopsis
rpminfo(string $path, bool $full = false, string &$error = ?): ?array
```

Вийняти інформацію про локальний файл RPM.

### Список параметрів

`path`

Шлях до файлу.

`full`

Якщо **`true`**, для файлу будуть вилучені всі заголовки. Інакше буде вилучено мінімальний набір.

`error`

Якщо заданий, то нього буде записана інформація про помилку, у разі її виникнення. Це дозволить уникнути попереджень під час виконання.

### Значення, що повертаються

Масив з даними або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**rpminfo()\*\*\*\*

```php
<?php
rpmaddtag(RPMTAG_BUILDTIME);
$info = rpminfo("./php-pecl-rpminfo-0.4.2-1.el8.remi.7.4.x86_64.rpm");
print_r($info);
?>
```

Результат виконання наведеного прикладу:

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

-   [rpmaddtag()](function.rpmaddtag.md) \- Додає тег, отриманий у запиті
