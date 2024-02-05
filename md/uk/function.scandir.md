---
navigation:
  - function.rewinddir.md: « rewinddir
  - book.fileinfo.md: FileInfo »
  - index.md: PHP Manual
  - ref.dir.md: Функції для роботи з каталогами
title: scandir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# scandir

(PHP 5, PHP 7, PHP 8)

scandir — Отримує список файлів і каталогів, які розташовані вказаним шляхом

### Опис

```methodsynopsis
scandir(string $directory, int $sorting_order = SCANDIR_SORT_ASCENDING, ?resource $context = null): array|false
```

Повертає масив (array), що містить імена файлів та каталогів, розташованих по дорозі, переданій у параметрі `directory`

### Список параметрів

`directory`

Сканований каталог.

`sorting_order`

За умовчанням сортування провадиться в алфавітному порядку за зростанням. Якщо необов'язковий параметр `sorting_order`установлен в значение\*\*`SCANDIR_SORT_DESCENDING`\*\*, сортування проводиться в алфавітному порядку за спаданням. Якщо ж він встановлений у значення **`SCANDIR_SORT_NONE`**, Сортування не проводиться.

`context`

За описанием параметра`context` зверніться до розділу [Потоки](ref.stream.md)данного руководства.

### Значення, що повертаються

Повертає масив (array) імен файлів у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Если`directory` не є каталогом, повертається **`false`** та генерується повідомлення про помилку рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Простий приклад використання функції **scandir()****

```php
<?php
$dir    = '/tmp';
$files1 = scandir($dir);
$files2 = scandir($dir, SCANDIR_SORT_DESCENDING);

print_r($files1);
print_r($files2);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => .
    [1] => ..
    [2] => bar.php
    [3] => foo.txt
    [4] => somedir
)
Array
(
    [0] => somedir
    [1] => foo.txt
    [2] => bar.php
    [3] => ..
    [4] => .
)
```

### Примітки

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Дивіться також

-   [opendir()](function.opendir.md) \- Відкриває дескриптор каталогу
-   [readdir()](function.readdir.md) \- Отримує елемент каталогу за його дескриптором
-   [glob()](function.glob.md) \- Знаходить файлові шляхи, що збігаються із шаблоном
-   [is\_dir()](function.is-dir.md) \- Визначає, чи є ім'я файлу директорією
-   [sort()](function.sort.md) \- Сортує масив за зростанням
