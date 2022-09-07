---
navigation:
  - ziparchive.open.md: '« ZipArchive::open'
  - ziparchive.registerprogresscallback.md: 'ZipArchive::registerProgressCallback »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::registerCancelCallback'
---
# ZipArchive::registerCancelCallback

(PHP >= 8.0.0, PECL zip >= 1.17.0)

ZipArchive::registerCancelCallback — Реєструє callback-функцію для дозволу скасування під час закриття архіву

### Опис

```methodsynopsis
public ZipArchive::registerCancelCallback(callable $callback): bool
```

Реєструє `callback`функцію для дозволу скасування під час закриття архіву.

### Список параметрів

`callback`

Якщо функція поверне 0, операція продовжиться, при іншому значенні її буде скасовано.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

У цьому прикладі створюється ZIP-архів php.zip і скасовується операція за певних умов запуску.

**Приклад #1 Архівація файлу**

```php
<?php
$zip = new ZipArchive();
if ($zip->open('php.zip', ZipArchive::CREATE | ZipArchive::OVERWRITE)) {
    $zip->addFile(PHP_BINARY, 'php');
    $zip->registerCancelCallback(function () {
        return ($someruncondition ? -1 : 0);
    });
    $zip->close();
}
```

### Примітки

> **Зауваження**
> 
> Функція доступна, якщо PHP скомпільовано з libzip ≥ 1.6.0.

### Дивіться також

-   [ZipArchive::registerProgressCallback()](ziparchive.registerprogresscallback.md) - Реєструє callback-функцію для надання оновлень під час закриття архіву
