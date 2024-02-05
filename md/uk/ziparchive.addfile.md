---
navigation:
  - ziparchive.addemptydir.md: '« ZipArchive::addEmptyDir'
  - ziparchive.addfromstring.md: 'ZipArchive::addFromString »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::addFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::addFile

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::addFile — Додає до ZIP-архіву файл за вказаним шляхом

### Опис

```methodsynopsis
public ZipArchive::addFile(    string $filepath,    string $entryname = "",    int $start = 0,    int $length = ZipArchive::LENGTH_TO_END,    int $flags = ZipArchive::FL_OVERWRITE): bool
```

Додає до ZIP-архіву файл по зазначеному шляху.

> **Зауваження**: Для максимальної переносимості, рекомендується завжди використовувати прямі сліші ( ) як роздільник директорій в іменах файлів.

### Список параметрів

`filepath`

Шлях до файлу для додавання.

`entryname`

Имя файла внутри ZIP-архива. Если указано, то переопределит параметр`filepath`

`start`

Початкова позиція для копіювання.

`length`

Довжина, яка має бути скопійована під час виконання операції часткового копіювання, якщо вказано значення **`ZipArchive::LENGTH_TO_END`** (0), буде використано розмір файлу, якщо вказано значення **`ZipArchive::LENGTH_UNCHECKED`**, буде використано весь файл (починаючи зі значення параметра `start`

`flags`

Бітова маска, що складається із значень: **`ZipArchive::FL_OVERWRITE`** **`ZipArchive::FL_ENC_GUESS`** **`ZipArchive::FL_ENC_UTF_8`** **`ZipArchive::FL_ENC_CP437`** \*\*`ZipArchive::FL_OPEN_FILE_NOW`\*\*Поведение констант описано на странице[ZIP-константи](zip.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 / 1.18.0 | Добавлен параметр`flags` |
| 8.3.0 / 1.22.1 | Добавлена константа\*\*`ZipArchive::FL_OPEN_FILE_NOW`\*\* |
| 8.3.0 / 1.22.2 | Додано константи, що задають значення довжини: **`ZipArchive::LENGTH_TO_END`**и**`ZipArchive::LENGTH_UNCHECKED`** |

### Приклади

У цьому прикладі відкривається файл ZIP-архіву test.zip і до нього додається файл /path/to/index.txt під ім'ям newname.txt.

**Приклад #1 Відкрити та додати**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    $zip->addFile('/path/to/index.txt', 'newname.txt');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

### Примітки

> **Зауваження** :
> 
> У процесі додавання файлу до архіву PHP заблокує файл. Розблокування відбудеться лише після закриття об'єкту [ZipArchive](class.ziparchive.md), шляхом виклику [ZipArchive::close()](ziparchive.close.md) або знищення об'єкта [ZipArchive](class.ziparchive.md). Це запобігає видаленню доданого до архіву файлу до того, як він буде розблокований.

### Дивіться також

-   [ZipArchive::replaceFile()](ziparchive.replacefile.md) \- Замінює файл у ZIP-архіві заданим шляхом
