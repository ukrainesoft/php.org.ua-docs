Додає авторизований відкритий ключ

-   [« ssh2\_poll](function.ssh2-poll.html)
    
-   [ssh2\_publickey\_init »](function.ssh2-publickey-init.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Додає авторизований відкритий ключ
    

# ssh2publickeyadd

(PECL ssh2> = 0.10)

ssh2publickeyadd — Додає авторизований відкритий ключ

### Опис

```methodsynopsis
ssh2_publickey_add(    resource $pkey,    string $algoname,    string $blob,    bool $overwrite = false,    array $attributes = ?): bool
```

> **Зауваження**: Підсистема відкритих ключів використовується для керування відкритими ключами на сервері, на якому клієнт *вже* пройшов авторизацію. Для авторизації за допомогою відкритого ключа на віддаленій системі, використовуйте натомість функцію [ssh2\_auth\_pubkey\_file()](function.ssh2-auth-pubkey-file.html)

### Список параметрів

`pkey`

Ресурс підсистеми відкритого ключа, створений за допомогою [ssh2\_publickey\_init()](function.ssh2-publickey-init.html)

`algoname`

Алгоритм ключа: ssh-dss, ssh-rsa

`blob`

Бінарний рядок, який містить відкритий ключ

`overwrite`

Чи потрібно перезаписати ключ, якщо він є?

`attributes`

Асоціативний масив атрибутів, які надаються відкритому ключу. Список атрибутів, що підтримуються, шукайте за словами "ietf-secsh-publickey-subsystem". Щоб вказати будь-який атрибут обов'язковим, поставте перед ім'ям зірочку. Якщо сервер не підтримує будь-який атрибут, позначений обов'язковим, це перерве процес додавання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додаємо відкритий ключ за допомогою **ssh2publickeyadd()****

```php
<?php
$ssh2 = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($ssh2, 'jdoe', 'password');
$pkey = ssh2_publickey_init($ssh2);

$keyblob = base64_decode('
AAAAB3NzaC1yc2EAAAABIwAAAIEA5HVt6VqSGd5PTrLRdjNONxXH1tVFGn0
Bd26BF0aCP9qyJRlvdJ3j4WBeX4ZmrveGrjMgkseSYc4xZ26sDHwfL351xj
zaLpipu\BGRrw17mWVBhuCExo476ri5tQFzbTc54VEHYckxQ16CjSTibI5X
69GmnYC9PNqEYq/1TP+HF10=');

ssh2_publickey_add($pkey, 'ssh-rsa', $keyblob, false, array('comment'=>"John's Key"));
?>
```

### Дивіться також

-   [ssh2\_publickey\_init()](function.ssh2-publickey-init.html) - Ініціалізує підсистему відкритого ключа
-   [ssh2\_publickey\_remove()](function.ssh2-publickey-remove.html) - Видаляє авторизований відкритий ключ
-   [ssh2\_publickey\_list()](function.ssh2-publickey-list.html) - Список вже авторизованих відкритих ключів