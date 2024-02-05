---
navigation:
  - ziparchive.renamename.md: '« ZipArchive::renameName'
  - ziparchive.setarchivecomment.md: 'ZipArchive::setArchiveComment »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::replaceFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::replaceFile

(PHP >= 8.0.0, PECL zip >= 1.18.0)

ZipArchive::replaceFile — Замінює файл у ZIP-архіві заданим шляхом

### Опис

```methodsynopsis
public ZipArchive::replaceFile(    string $filepath,    int $index,    int $start = 0,    int $length = ZipArchive::LENGTH_TO_END,    int $flags = 0): bool
```

Замінює файл у ZIP-архіві заданим шляхом.

> **Зауваження**: Для максимальної переносимості, рекомендується завжди використовувати прямі сліші ( ) як роздільник директорій в іменах файлів.

### Список параметрів

`filepath`

Шлях до файлу для додавання.

`index`

Індекс файлу, що замінюється, його ім'я не змінюється.

`start`

Початкова позиція для копіювання.

`length`

Довжина, яка має бути скопійована під час виконання операції часткового копіювання, якщо вказано значення **`ZipArchive::LENGTH_TO_END`** (0), буде використано розмір файлу, якщо вказано значення **`ZipArchive::LENGTH_UNCHECKED`**, буде використано весь файл (починаючи зі значення параметра `start`

`flags`

Бітова маска, що складається із значень: **`ZipArchive::FL_ENC_GUESS`** **`ZipArchive::FL_ENC_UTF_8`** **`ZipArchive::FL_ENC_CP437`** **`ZipArchive::FL_OPEN_FILE_NOW`**. Поведінка цих констант описана на сторінці [Константи ZIP](zip.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 / 1.22.1 | Добавлена константа\*\*`ZipArchive::FL_OPEN_FILE_NOW`\*\* |
| 8.3.0 / 1.22.2 | Додано константи, що задають значення довжини: **`ZipArchive::LENGTH_TO_END`** і **`ZipArchive::LENGTH_UNCHECKED`** |

### Приклади

У цьому прикладі відкривається ZIP-архів test.zip і запис із індексом 1 замінюється на шлях /path/to/index.txt.

**Приклад #1 Відкриття та заміна**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    $zip->replaceFile('/path/to/index.txt', 1);
    $zip->close();
    echo 'Ок';
} else {
    echo 'Ошибка';
}
?>
```

### Дивіться також

-   [ZipArchive::addFile()](ziparchive.addfile.md) \- Додає до ZIP-архіву файл по зазначеному шляху
