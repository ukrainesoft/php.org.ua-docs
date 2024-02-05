---
navigation:
  - function.getcwd.md: « getcwd
  - function.readdir.md: readdir »
  - index.md: PHP Manual
  - ref.dir.md: Функції для роботи з каталогами
title: opendir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# opendir

(PHP 4, PHP 5, PHP 7, PHP 8)

opendir — Відкриває дескриптор каталогу

### Опис

```methodsynopsis
opendir(string $directory, ?resource $context = null): resource|false
```

Відкриває дескриптор каталогу для подальшого використання з функціями [closedir()](function.closedir.md) [readdir()](function.readdir.md) і [rewinddir()](function.rewinddir.md)

### Список параметрів

`directory`

Шлях до каталогу

`context`

Для описания параметра`context` зверніться до розділу [Потоки](ref.stream.md)

### Значення, що повертаються

Повертає дескриптор каталогу (resource) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

Може статися, якщо `directory` не є директорією, директорія не може бути відкрита через недостатні дозволи або помилки файлової системи.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад использования функции**opendir()\*\*\*\*

```php
<?php
$dir = "/etc/php5/";

// Открыть известный каталог и начать считывать его содержимое
if (is_dir($dir)) {
    if ($dh = opendir($dir)) {
        while (($file = readdir($dh)) !== false) {
            echo "файл: $file : тип: " . filetype($dir . $file) . "\n";
        }
        closedir($dh);
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
файл: . : тип: dir
файл: .. : тип: dir
файл: apache : тип: dir
файл: cgi : тип: dir
файл: cli : тип: dir
```

### Дивіться також

-   [is\_dir()](function.is-dir.md) \- Визначає, чи є ім'я файлу директорією
-   [readdir()](function.readdir.md) \- Отримує елемент каталогу за його дескриптором
-   [dir()](function.dir.md) \- Повертає екземпляр класу Directory
