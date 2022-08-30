Відкриває дескриптор каталогу

-   [« getcwd](function.getcwd.html)
    
-   [readdir »](function.readdir.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з каталогами](ref.dir.html)
    
-   Відкриває дескриптор каталогу
    

# opendir

(PHP 4, PHP 5, PHP 7, PHP 8)

opendir — Відкриває дескриптор каталогу

### Опис

```methodsynopsis
opendir(string $directory, ?resource $context = null): resource|false
```

Відкриває дескриптор каталогу для подальшого використання з функціями [closedir()](function.closedir.html) [readdir()](function.readdir.html) і [rewinddir()](function.rewinddir.html)

### Список параметрів

`directory`

Шлях до каталогу

`context`

Для опису параметра `context` зверніться до розділу [Потоки](ref.stream.html)

### Значення, що повертаються

Повертає дескриптор каталогу (resource) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

Може статися, якщо `directory` не є директорією, директорія не може бути відкрита через недостатні дозволи або помилки файлової системи.

### список змін

| Версия | Описание |
| --- | --- |
|  | `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання функції **opendir()****

```php
<?php
$dir = "/etc/php5/";

// Открыть известный каталог и начать считывать его содержимое
if (is_dir($dir)) {
    if ($dh = opendir($dir)) {
        while (($file = readdir($dh)) !== false) {
            echo "файл: $file : тип: " . filetype($dir . $file) . "\n";
        }
        closedir($dh);
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
файл: . : тип: dir
файл: .. : тип: dir
файл: apache : тип: dir
файл: cgi : тип: dir
файл: cli : тип: dir
```

### Дивіться також

-   [ісdir()](function.is-dir.html) - Визначає, чи є ім'я файлу директорією
-   [readdir()](function.readdir.html) - Отримує елемент каталогу за його дескриптором
-   [dir()](function.dir.html) - Повертає екземпляр класу Directory