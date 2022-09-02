---
navigation:
  - function.chmod.md: « chmod
  - function.clearstatcache.md: clearstatcache »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: chown
---
# chown

(PHP 4, PHP 5, PHP 7, PHP 8)

chown — Змінює власника файлу

### Опис

```methodsynopsis
chown(string $filename, string|int $user): bool
```

Здійснює спробу зміни власника файлу з ім'ям `filename` на власника, чиє ім'я передано у параметрі `user` (у вигляді числа чи рядка). Тільки суперкористувач може змінювати власника файлу.

### Список параметрів

`filename`

Шлях до файлу.

`user`

Ім'я користувача чи число.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад простого використання **chown()****

```php
<?php

// Используемое имя файла и имя пользователя
$file_name= "foo.php";
$path = "/home/sites/php.net/public_html/sandbox/" . $file_name ;
$user_name = "root";

// Устанавливаем пользователя
chown($path, $user_name);

// Проверяем результат
$stat = stat($path);
print_r(posix_getpwuid($stat['uid']));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [name] => root
    [passwd] => x
    [uid] => 0
    [gid] => 0
    [gecos] => root
    [dir] => /root
    [shell] => /bin/bash
)
```

### Примітки

> **Зауваження**: Ця функція не застосовується для роботи з [віддаленими файлами](features.remote-files.md)оскільки файл повинен бути доступний через файлову систему сервера.

> **Зауваження**: У Windows функція мовчки завершується помилкою при застосуванні до звичайного файлу.

### Дивіться також

-   [chmod()](function.chmod.md) - Змінює режим доступу до файлу
-   [chgrp()](function.chgrp.md) - Змінює групу файлу
