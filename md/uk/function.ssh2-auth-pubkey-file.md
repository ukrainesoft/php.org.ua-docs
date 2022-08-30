Аутентифікація з відкритим ключем

-   [« ssh2authpassword](function.ssh2-auth-password.html)
    
-   [ssh2connect »](function.ssh2-connect.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SSH2](ref.ssh2.md)
    
-   Аутентифікація з відкритим ключем
    

# ssh2authpubkeyfile

(PECL ssh2> = 0.9.0)

ssh2authpubkeyfile — Аутентифікація з відкритим ключем

### Опис

```methodsynopsis
ssh2_auth_pubkey_file(    resource $session,    string $username,    string $pubkeyfile,    string $privkeyfile,    string $passphrase = ?): bool
```

Аутентифікація з відкритим ключем, збереженим у файлі.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2connect()](function.ssh2-connect.html)

`username`

`pubkeyfile`

Відкритий ключ у форматі OpenSSH. Має виглядати приблизно так:

ssh-rsa AAAAB3NzaC1yc2EAAA....NX6sqSnHA8= rsa-key-20121110

`privkeyfile`

`passphrase`

Якщо `privkeyfile` зашифрований (як би мав), то необхідно надати `passphrase`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Аутентифікація з відкритим ключем**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22, array('hostkey'=>'ssh-rsa'));

if (ssh2_auth_pubkey_file($connection, 'username',
                          '/home/username/.ssh/id_rsa.pub',
                          '/home/username/.ssh/id_rsa', 'secret')) {
  echo "Успешная аутентификация с открытым ключом\n";
} else {
  die('Неудачная аутентификация с открытым ключом');
}
?>
```

### Примітки

> **Зауваження**
> 
> Основна бібліотека libssh не підтримує часткові автентифікації дуже чисто. Тобто, якщо вам потрібно надати як відкритий ключ, так і пароль, він виглядатиме так, якби ця функція зазнала невдачі. У цьому випадку невдалий виклик може означати, що автентифікація не завершена. Вам потрібно ігнорувати це невдале виконання, продовжити роботу та викликати [ssh2authpassword()](function.ssh2-auth-password.html) для завершення автентифікації.