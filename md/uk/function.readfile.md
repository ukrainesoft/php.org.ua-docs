---
navigation:
  - function.popen.md: « popen
  - function.readlink.md: readlink »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: readfile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readfile

(PHP 4, PHP 5, PHP 7, PHP 8)

readfile — Виводить файл

### Опис

```methodsynopsis
readfile(string $filename, bool $use_include_path = false, ?resource $context = null): int|false
```

Читає файл та записує його у буфер виводу.

### Список параметрів

`filename`

Ім'я файлу, що читається.

`use_include_path`

Якщо ви хочете, щоб використовувався пошук файлу в [include\_path](ini.core.md#ini.include-path), встановіть цей параметр у **`true`**

`context`

Ресурс (resource) с[контекстом потоку](stream.contexts.md)

### Значення, що повертаються

Повертає кількість прочитаних із файлу байт у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Примусове завантаження за допомогою **readfile()****

```php
<?php
$file = 'monkey.gif';

if (file_exists($file)) {
    header('Content-Description: File Transfer');
    header('Content-Type: application/octet-stream');
    header('Content-Disposition: attachment; filename="'.basename($file).'"');
    header('Expires: 0');
    header('Cache-Control: must-revalidate');
    header('Pragma: public');
    header('Content-Length: ' . filesize($file));
    readfile($file);
    exit;
}
?>
```

Висновок наведеного прикладу буде схожим на:

![Діалог відкриття / збереження файлу](images/e88cefb5c3fca5060e2490b9763c4433-readfile.png)

### Примітки

> **Зауваження** :
> 
> **readfile()** сама по собі не призводить до будь-яких проблем з пам'яттю, навіть при надсиланні великих файлів. У разі помилки перевищення пам'яті переконайтеся, що буферизація виводу вимкнена за допомогою [ob\_get\_level()](function.ob-get-level.md)

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Дивіться також

-   [fpassthru()](function.fpassthru.md) \- Виводить всі дані з файлового покажчика, що залишилися.
-   [file()](function.file.md) \- Читає вміст файлу та поміщає його в масив
-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [include](function.include.md) \- include
-   [require](function.require.md) \- require
-   [virtual()](function.virtual.md) \- Виконує підзапит Apache
-   [file\_get\_contents()](function.file-get-contents.md) \- Читає вміст файлу в рядок
-   [Підтримувані протоколи та обгортки](wrappers.md)
