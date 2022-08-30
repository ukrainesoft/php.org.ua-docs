Додає до ZIP-архіву файл за вказаним шляхом

-   [« ZipArchive::addEmptyDir](ziparchive.addemptydir.html)
    
-   [ZipArchive::addFromString »](ziparchive.addfromstring.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Додає до ZIP-архіву файл за вказаним шляхом
    

# ZipArchive::addFile

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::addFile — Додає до ZIP-архіву файл за вказаним шляхом

### Опис

```methodsynopsis
public ZipArchive::addFile(    string $filepath,    string $entryname = "",    int $start = 0,    int $length = 0,    int $flags = ZipArchive::FL_OVERWRITE): bool
```

Додає до ZIP-архіву файл по зазначеному шляху.

> **Зауваження**: Для максимальної переносимості, рекомендується завжди використовувати прямі сліші (`/`) як роздільник директорій в іменах файлів.

### Список параметрів

`filepath`

Шлях до файлу для додавання.

`entryname`

Ім'я файлу всередині ZIP-архіву. Якщо вказано, то перевизначить `filepath`

`start`

Для часткового копіювання є початкова позиція.

`length`

Для часткового копіювання - довжина файлу, що копіюється, якщо 0 або -1, використовується весь файл (починаючи з `start`

`flags`

Бітова маска, що складається з **`ZipArchive::FL_OVERWRITE`** **`ZipArchive::FL_ENC_GUESS`** **`ZipArchive::FL_ENC_UTF_8`** **`ZipArchive::FL_ENC_CP437`**. Поведінка констант описана на сторінці [ZIP-константи](zip.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `flags` |

### Приклади

У цьому прикладі відкривається файл ZIP-архіву test.zip і до нього додається файл /path/to/index.txt під ім'ям newname.txt.

**Приклад #1 Відкрити та додати**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    $zip->addFile('/path/to/index.txt', 'newname.txt');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

### Примітки

> **Зауваження**
> 
> У процесі додавання файлу до архіву PHP заблокує файл. Розблокування відбудеться лише після закриття об'єкту [ZipArchive](class.ziparchive.html), шляхом виклику [ZipArchive::close()](ziparchive.close.html) або знищення об'єкта [ZipArchive](class.ziparchive.html). Це запобігає видаленню доданого до архіву файлу до того, як він буде розблокований.

### Дивіться також

-   [ZipArchive::replaceFile()](ziparchive.replacefile.html) - Замінює файл у ZIP-архіві вказаним шляхом