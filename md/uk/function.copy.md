Копіює файл

-   [« clearstatcache](function.clearstatcache.html)
    
-   [delete »](function.delete.html)
    
-   [PHP Manual](index.html)
    
-   [Функції файлової системи](ref.filesystem.html)
    
-   Копіює файл
    

# copy

(PHP 4, PHP 5, PHP 7, PHP 8)

copy — Копіює файл

### Опис

```methodsynopsis
copy(string $from, string $to, ?resource $context = null): bool
```

Копіює файл `from` у файл з ім'ям `to`

Якщо потрібно перейменувати файл, використовуйте функцію [rename()](function.rename.html)

### Список параметрів

`from`

Шлях до вихідного файлу.

`to`

Шлях до цільового файлу. Якщо `to` є URL, то копіювання може завершитися помилкою, якщо обгортка URL не підтримує перезаписування існуючих файлів.

**Увага**

Якщо цільовий файл вже існує, він буде перезаписаний.

`context`

Коректний ресурс контексту, створений функцією [streamcontextcreate()](function.stream-context-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання функції **copy()****

```php
<?php
$file = 'example.txt';
$newfile = 'example.txt.bak';

if (!copy($file, $newfile)) {
    echo "не удалось скопировать $file...\n";
}
?>
```

### Дивіться також

-   [moveuploadedfile()](function.move-uploaded-file.html) - Переміщує завантажений файл у нове місце
-   [rename()](function.rename.html) - Перейменовує файл або директорію
-   Розділ керівництва[Завантаження файлів](features.file-upload.html)"