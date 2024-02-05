---
navigation:
  - function.ssh2-auth-password.md: « ssh2\_auth\_password
  - function.ssh2-connect.md: ssh2\_connect »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_auth\_pubkey\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_auth\_pubkey\_file

(PECL ssh2 >= 0.9.0)

ssh2\_auth\_pubkey\_file — Аутентифікація з відкритим ключем

### Опис

```methodsynopsis
ssh2_auth_pubkey_file(    resource $session,    string $username,    string $pubkeyfile,    string $privkeyfile,    string $passphrase = ?): bool
```

Аутентифікація з відкритим ключем, збереженим у файлі.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`username`

`pubkeyfile`

Відкритий ключ у форматі OpenSSH. Має виглядати приблизно так:

ssh-rsa AAAAB3NzaC1yc2EAAA....NX6sqSnHA8= rsa-key-20121110

`privkeyfile`

`passphrase`

Якщо `privkeyfile` зашифрований (як би мав), то необхідно надати `passphrase`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Аутентифікація з відкритим ключем**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22, array('hostkey'=>'ssh-rsa'));

if (ssh2_auth_pubkey_file($connection, 'username',
                          '/home/username/.ssh/id_rsa.pub',
                          '/home/username/.ssh/id_rsa', 'secret')) {
  echo "Успешная аутентификация с открытым ключом\n";
} else {
  die('Неудачная аутентификация с открытым ключом');
}
?>
```

### Примітки

> **Зауваження** :
> 
> Основна бібліотека libssh не підтримує часткові автентифікації дуже чисто. Тобто, якщо вам потрібно надати як відкритий ключ, так і пароль, він виглядатиме так, якби ця функція зазнала невдачі. У цьому випадку невдалий виклик може означати, що автентифікація не завершена. Вам потрібно ігнорувати це невдале виконання, продовжити роботу та викликати [ssh2\_auth\_password()](function.ssh2-auth-password.md) для завершення автентифікації.
