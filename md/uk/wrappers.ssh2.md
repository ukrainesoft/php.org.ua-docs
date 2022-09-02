---
navigation:
  - wrappers.phar.md: '« phar://'
  - wrappers.rar.md: 'rar:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'ssh2://'
---
# ssh2://

ssh2:// - Secure Shell 2

### Опис

ssh2.shell:// ssh2.exec:// ssh2.tunnel:// ssh2.sftp:// ssh2.scp:// (PECL)

> **Зауваження** **Ця обгортка не включена за замовчуванням**  
> Для того щоб використовувати обгортки ssh2.:// вам необхідно встановити модуль [» SSH2](https://pecl.php.net/package/ssh2), доступний у репозиторії [» PECL](https://pecl.php.net/)

Крім отримання традиційних даних для входу до URI, обгортки ssh2 також повторно використовувати відкриті з'єднання, передаючи ресурс з'єднання в хост-частину URL.

### Використання

-   сш2.шелл://усер:[pass@example.com](mailto:pass@example.com):22/xterm
-   ssh2.exec://user:[pass@example.com](mailto:pass@example.com):22/usr/local/bin/somecmd
-   ssh2.tunnel://user:[pass@example.com](mailto:pass@example.com)
-   ssh2.s[ftp://user:pass@example.com:22/path/to/filename](ftp://user:pass@example.com:22/path/to/filename)

### Опції

**Основна інформація**

| Атрибут | ssh2.shell | ssh2.exec | ssh2.tunnel | ssh2.sftp | ssh2.scp |
| --- | --- | --- | --- | --- | --- |
| Обмеження по [allowurlfopen](filesystem.configuration.md#ini.allow-url-fopen) | Так | Так | Так | Так | Так |
| Читання | Так | Так | Так | Так | Так |
| Запис | Так | Так | Так | Так | Ні |
| Додавання | Ні | Ні | Ні | Так (коли підтримується сервером) | Ні |
| Одночасне читання та запис | Так | Так | Так | Так | Ні |
| Підтримка [stat()](function.stat.md) | Ні | Ні | Ні | Так | Ні |
| Підтримка [unlink()](function.unlink.md) | Ні | Ні | Ні | Так | Ні |
| Підтримка [rename()](function.rename.md) | Ні | Ні | Ні | Так | Ні |
| Підтримка [mkdir()](function.mkdir.md) | Ні | Ні | Ні | Так | Ні |
| Підтримка [rmdir()](function.rmdir.md) | Ні | Ні | Ні | Так | Ні |

**Опції контексту**

| Имя | Использование | По умолчанию |
| --- | --- | --- |
| `session` | Попередньо з'єднаний ресурс ssh2 для повторного використання |  |
| `sftp` | Попередньо виділений ресурс sftp для повторного використання |  |
| `methods` | Обмін ключами, ключ хоста, шифр, компресія та методи MAC для використання |  |
| `callbacks` |  |  |
| `username` | Ім'я користувача для з'єднання |  |
| `password` | Пароль для автентифікації |  |
| `pubkey_file` | Ім'я файлу, в якому знаходиться відкритий ключ для автентифікації |  |
| `privkey_file` | Ім'я файлу, в якому знаходиться приватний ключ для автентифікації |  |
| `env` | Асоціативний масив зі змінними оточеннями, які необхідно встановити |  |
| `term` | Тип емуляції терміналу для запиту, коли виділяється pty |  |
| `term_width` | Ширина терміналу, запитується коли виділяється pty |  |
| `term_height` | Висота терміналу, запитується коли виділяється pty |  |
| `term_units` | Одиниці, в яких вимірюються termwidth та termheight | **`SSH2_TERM_UNIT_CHARS`** |

### Приклади

**Приклад #1 Відкриття потоку з активного з'єднання**

```php
<?php
$session = ssh2_connect('example.com', 22);
ssh2_auth_pubkey_file($session, 'username', '/home/username/.ssh/id_rsa.pub',
                                            '/home/username/.ssh/id_rsa', 'secret');
$stream = fopen("ssh2.tunnel://$session/remote.example.com:1234", 'r');
?>
```

**Приклад #2 Змінна $session має бути доступною!**

Якщо ви хочете використовувати будь-яку обгортку ssh2.://$session, необхідно зберегти доступним ресурс, що зберігається в змінній $session. Наступний код не матиме бажаного ефекту:

```php
<?php
$session = ssh2_connect('example.com', 22);
ssh2_auth_pubkey_file($session, 'username', '/home/username/.ssh/id_rsa.pub',
                                            '/home/username/.ssh/id_rsa', 'secret');
$connection_string = "ssh2.sftp://$session/";
unset($session);
$stream = fopen($connection_string . "path/to/file", 'r');
?>
```

unset() закриває сесію, тому що $connectionstring не є посиланням на змінну $session, лише її текстовим уявленням. Це також відбувається і у разі неявного виклику [unset()](function.unset.md) при виході з області видимості (наприклад, функції).
