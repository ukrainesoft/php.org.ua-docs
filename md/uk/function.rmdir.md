Видаляє директорію

-   [« rewind](function.rewind.html)
    
-   [setfilebuffer »](function.set-file-buffer.html)
    
-   [PHP Manual](index.html)
    
-   [Функції файлової системи](ref.filesystem.html)
    
-   Видаляє директорію
    

# rmdir

(PHP 4, PHP 5, PHP 7, PHP 8)

rmdir - Видаляє директорію

### Опис

```methodsynopsis
rmdir(string $directory, ?resource $context = null): bool
```

Намагається видалити директорію з ім'ям `directory`. Директорія має бути порожньою і повинні мати необхідні для цього права. При невдалому виконанні буде згенеровано помилку рівня **`E_WARNING`**

### Список параметрів

`directory`

Шлях до директорії.

`context`

Ресурс (resource) з [контекстом потоку](stream.contexts.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **rmdir()****

```php
<?php
if (!is_dir('examples')) {
    mkdir('examples');
}

rmdir('examples');
?>
```

### Дивіться також

-   [ісdir()](function.is-dir.html) - Визначає, чи є ім'я файлу директорією
-   [mkdir()](function.mkdir.html) - створює директорію
-   [unlink()](function.unlink.html) - Видаляє файл