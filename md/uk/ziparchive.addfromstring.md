---
navigation:
  - ziparchive.addfile.md: '« ZipArchive::addFile'
  - ziparchive.addglob.md: 'ZipArchive::addGlob »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::addFromString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::addFromString

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::addFromString — Додає файл до ZIP-архіву, використовуючи його вміст

### Опис

```methodsynopsis
public ZipArchive::addFromString(string $name, string $content, int $flags = ZipArchive::FL_OVERWRITE): bool
```

Додає файл до ZIP-архіву, використовуючи його вміст.

> **Зауваження**: Для максимальної переносимості, рекомендується завжди використовувати прямі сліші ( ) як роздільник директорій в іменах файлів.

### Список параметрів

`name`

Локальне ім'я для створення файлу.

`content`

Вміст для створення файлу. Використовується у двійковому безпечному режимі.

`flags`

Бітова маска, що складається з **`ZipArchive::FL_OVERWRITE`** **`ZipArchive::FL_ENC_GUESS`** **`ZipArchive::FL_ENC_UTF_8`** \*\*`ZipArchive::FL_ENC_CP437`\*\*Поведение констант описано на странице[ZIP-константи](zip.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 / 1.18.0 | Добавлен параметр`flags` |

### Приклади

**Приклад #1 Додати запис до нового архіву**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip', ZipArchive::CREATE);
if ($res === TRUE) {
    $zip->addFromString('test.txt', 'здесь следует содержимое файла');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

**Приклад #2 Додати файл до директорії всередині архіву**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    $zip->addFromString('dir/test.txt', 'здесь следует содержимое файла');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```
