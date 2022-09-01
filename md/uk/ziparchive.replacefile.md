---
navigation:
  - ziparchive.renamename.md: '« ZipArchive::renameName'
  - ziparchive.setarchivecomment.md: 'ZipArchive::setArchiveComment »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::replaceFile'
---
# ZipArchive::replaceFile

(PHP >= 8.0.0, PECL zip >= 1.18.0)

ZipArchive::replaceFile — Замінює файл у ZIP-архіві вказаним шляхом

### Опис

```methodsynopsis
public ZipArchive::replaceFile(    string $filepath,    int $index,    int $start = 0,    int $length = 0,    int $flags = 0): bool
```

Замінює файл у ZIP-архіві вказаним шляхом.

> **Зауваження**: Для максимальної переносимості, рекомендується завжди використовувати прямі сліші (`/`) як роздільник директорій в іменах файлів.

### Список параметрів

`filepath`

Шлях до файлу для додавання.

`index`

Індекс файлу, що підлягає заміні, його ім'я не змінюється.

`start`

Для часткового копіювання є початкова позиція.

`length`

Для часткового копіювання - довжина, яку потрібно скопіювати, якщо 0 або -1, використовується весь файл (починаючи з `start`

`flags`

Бітова маска, що складається з **`ZipArchive::FL_ENC_GUESS`** **`ZipArchive::FL_ENC_UTF_8`** **`ZipArchive::FL_ENC_CP437`**. Поведінка цих констант описана на сторінці [Константи ZIP](zip.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

У цьому прикладі відкривається ZIP-архів test.zip та замінюється запис з індексом 1 на /path/to/index.txt.

**Приклад #1 Відкриття та заміна**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    $zip->replaceFile('/path/to/index.txt', 1);
    $zip->close();
    echo 'Ок';
} else {
    echo 'Ошибка';
}
?>
```

### Дивіться також

-   [ZipArchive::addFile()](ziparchive.addfile.md) - Додає до ZIP-архіву файл по зазначеному шляху
