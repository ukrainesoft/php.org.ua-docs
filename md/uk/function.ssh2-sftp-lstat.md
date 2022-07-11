- [« ssh2_sftp_chmod](function.ssh2-sftp-chmod.md)
- [ssh2_sftp_mkdir »](function.ssh2-sftp-mkdir.md)

- [PHP Manual](index.md)
- [Функції SSH2](ref.ssh2.md)
- Інформація про символічне посилання

# ssh2_sftp_lstat

(PECL ssh2 \>= 0.9.0)

ssh2_sftp_lstat — Інформація про символічне посилання

### Опис

**ssh2_sftp_lstat**(resource `$sftp`, string `$path`): array

Інформація про символічне посилання на серверній файловій системі *без*
переходу нею.

Ця функція аналогічна використанню функції
[lstat()](function.lstat.md) з обгорткою
[ssh2.sftp://](wrappers.ssh2.md) і повертає такі самі значення.

### Список параметрів

`sftp`
Ресурс SSH2 SFTP, відкритий за допомогою
[ssh2_sftp()](function.ssh2-sftp.md).

`path`
Шлях до символічного посилання.

### Значення, що повертаються

Список значень, що повертаються дивіться в описі функції
[stat()](function.stat.md).

### Приклади

**Приклад #1 Інформація про символічне посилання**

` <?php$connection = ssh2_connect('shell.example.com', 22);ssh2_auth_password($connection, 'username', 'password');$sftp = ssh2_sftp($connection);$statinfo = ssh2 , '/path/to/symlink');$filesize = $statinfo['size'];$group = $statinfo['gid'];$owner = $statinfo['uid'];$atime = $statinfo[ 'atime'];$mtime = $statinfo['mtime'];$mode = $statinfo['mode'];?> `

### Дивіться також

- [ssh2_sftp_stat()](function.ssh2-sftp-stat.md) - Інформація про
файлі
- [lstat()](function.lstat.md) - Повертає інформацію про файл або
символічне посилання
- [stat()](function.stat.md) - Повертає інформацію про файл
