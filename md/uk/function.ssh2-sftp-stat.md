- [« ssh2_sftp_rmdir](function.ssh2-sftp-rmdir.md)
- [ssh2_sftp_symlink »](function.ssh2-sftp-symlink.md)

- [PHP Manual](index.md)
- [Функції SSH2](ref.ssh2.md)
- Інформація про файл

# ssh2_sftp_stat

(PECL ssh2 \>= 0.9.0)

ssh2_sftp_stat — Інформація про файл

### Опис

**ssh2_sftp_stat**(resource `$sftp`, string `$path`): array

Інформація про файл на сервері з урахуванням символічних посилань.

Функція працює аналогічно [stat()](function.stat.md) з обгорткою
[ssh2.sftp://](wrappers.ssh2.md) і повертає такі самі значення.

### Список параметрів

`sftp`
Ресурс SSH2 SFTP, відкритий за допомогою
[ssh2_sftp()](function.ssh2-sftp.md).

`path`

### Значення, що повертаються

Список значень, що повертаються дивіться в описі функції
[stat()](function.stat.md).

### Приклади

**Приклад #1 Інформація про файл**

` <?php$connection = ssh2_connect('shell.example.com', 22);ssh2_auth_password($connection, 'username', 'password');$sftp = ssh2_sftp($connection);$statinfo = ssh$ , '/path/to/file');$filesize = $statinfo['size'];$group = $statinfo['gid'];$owner = $statinfo['uid'];$atime = $statinfo[ 'atime'];$mtime = $statinfo['mtime'];$mode = $statinfo['mode'];?> `

### Дивіться також

- [ssh2_sftp_lstat()](function.ssh2-sftp-lstat.md) - Інформація про
символічне посилання
- [lstat()](function.lstat.md) - Повертає інформацію про файл або
символічне посилання
- [stat()](function.stat.md) - Повертає інформацію про файл
