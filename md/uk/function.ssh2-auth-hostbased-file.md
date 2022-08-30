Аутентифікація з використанням відкритого ключа хоста

-   [« ssh2authagent](function.ssh2-auth-agent.html)
    
-   [ssh2authnone »](function.ssh2-auth-none.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SSH2](ref.ssh2.md)
    
-   Аутентифікація з використанням відкритого ключа хоста
    

# ssh2authhostbasedfile

(PECL ssh2> = 0.9.0)

ssh2authhostbasedfile — Аутентифікація за допомогою відкритого ключа хоста

### Опис

```methodsynopsis
ssh2_auth_hostbased_file(    resource $session,    string $username,    string $hostname,    string $pubkeyfile,    string $privkeyfile,    string $passphrase = ?,    string $local_username = ?): bool
```

Аутентифікація за допомогою відкритого ключа хоста, збереженого у файлі.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2connect()](function.ssh2-connect.html)

`username`

`hostname`

`pubkeyfile`

`privkeyfile`

`passphrase`

Якщо `privkeyfile` зашифрований (як повинен), необхідно надати кодову фразу.

`local_username`

Якщо параметр `local_username` не заданий, буде використано значення з `username`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Аутентифікація за відкритим ключем**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22, array('hostkey'=>'ssh-rsa'));

if (ssh2_auth_hostbased_file($connection, 'remoteusername', 'myhost.example.com',
                             '/usr/local/etc/hostkey_rsa.pub',
                             '/usr/local/etc/hostkey_rsa', 'secret',
                             'localusername')) {
  echo "Успешная Hostbased-аутентификация по открытому ключу\n";
} else {
  die('Неудачная Hostbased-аутентификация по открытому ключу');
}
?>
```

### Примітки

> **Зауваження**
> 
> **ssh2authhostbasedfile()** вимагає libssh2 >= 0.7 та PHP/SSH2 >= 0.7