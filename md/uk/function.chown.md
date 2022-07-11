- [«chmod](function.chmod.md)
- [clearstatcache »](function.clearstatcache.md)

- [PHP Manual](index.md)
- [Функції файлової системи](ref.filesystem.md)
- Змінює власника файлу

# chown

(PHP 4, PHP 5, PHP 7, PHP 8)

chown — Змінює власника файлу

### Опис

**chown**(string `$filename`, string\|int `$user`): bool

Здійснює спробу зміни власника файлу з ім'ям `filename` на
власника, чиє ім'я передано в параметрі `user` (у вигляді чи
рядки). Тільки суперкористувач може змінювати власника файлу.

### Список параметрів

`filename`
Шлях до файлу.

`user`
Ім'я користувача чи число.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад простого використання **chown()****

` <?php// Використовуване ім'я файла і ім'япользователя$file_name= "foo.php";$path = "/home/sites/php.net/public_html/sandbox/" . $file_name ;$user_name = "root";// Встановлюємо користувачаchown($path, $user_name);// Перевіряємо результат$stat = stat($path);print_r(posix_getpwuid($stat['uid'] > `

Результатом виконання цього прикладу буде щось подібне:

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

### Примітки

> **Примітка**: Ця функція не застосовується для роботи з [віддаленими > файлами](features.remote-files.md), оскільки файл має бути
> доступний через файлову систему сервера.

> **Примітка**: У Windows функція мовчки завершується помилкою при
> застосування до звичайного файлу.

### Дивіться також

- [chmod()](function.chmod.md) - Змінює режим доступу до файлу
- [chgrp()](function.chgrp.md) - Змінює групу файлу
