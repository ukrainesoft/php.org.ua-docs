---
navigation:
  - class.ziparchive.md: « ZipArchive
  - ziparchive.addfile.md: 'ZipArchive::addFile »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::addEmptyDir'
---
# ZipArchive::addEmptyDir

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.8.0)

ZipArchive::addEmptyDir — Додає нову директорію

### Опис

```methodsynopsis
public ZipArchive::addEmptyDir(string $dirname, int $flags = 0): bool
```

Додає порожню директорію до архіву.

### Список параметрів

`dirname`

Директорія додавання.

`flags`

Бітова маска, що складається з **`ZipArchive::FL_ENC_GUESS`** **`ZipArchive::FL_ENC_UTF_8`** **`ZipArchive::FL_ENC_CP437`**. Поведінка констант описана на сторінці [ZIP-константи](zip.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `flags` |

### Приклади

**Приклад #1 Створення нової директорії у архіві.**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    if($zip->addEmptyDir('newDirectory')) {
        echo 'Создана новая директория';
    } else {
        echo 'Невозможно создать директорию';
    }
    $zip->close();
} else {
    echo 'ошибка';
}
?>
```
