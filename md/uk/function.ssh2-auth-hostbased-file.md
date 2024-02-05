---
navigation:
  - function.ssh2-auth-agent.md: « ssh2\_auth\_agent
  - function.ssh2-auth-none.md: ssh2\_auth\_none »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_auth\_hostbased\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_auth\_hostbased\_file

(PECL ssh2 >= 0.9.0)

ssh2\_auth\_hostbased\_file — Аутентифікація за допомогою відкритого ключа хоста

### Опис

```methodsynopsis
ssh2_auth_hostbased_file(    resource $session,    string $username,    string $hostname,    string $pubkeyfile,    string $privkeyfile,    string $passphrase = ?,    string $local_username = ?): bool
```

Аутентифікація за допомогою відкритого ключа хоста, збереженого у файлі.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`username`

`hostname`

`pubkeyfile`

`privkeyfile`

`passphrase`

Якщо `privkeyfile` зашифрований (як повинен), необхідно надати кодову фразу.

`local_username`

Якщо параметр `local_username`не задан, будет использовано значение из`username`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Аутентифікація за відкритим ключем**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22, array('hostkey'=>'ssh-rsa'));

if (ssh2_auth_hostbased_file($connection, 'remoteusername', 'myhost.example.com',
                             '/usr/local/etc/hostkey_rsa.pub',
                             '/usr/local/etc/hostkey_rsa', 'secret',
                             'localusername')) {
  echo "Успешная Hostbased-аутентификация по открытому ключу\n";
} else {
  die('Неудачная Hostbased-аутентификация по открытому ключу');
}
?>
```

### Примітки

> **Зауваження** :
> 
> **ssh2\_auth\_hostbased\_file()** вимагає libssh2 >= 0.7 та PHP/SSH2 >= 0.7
