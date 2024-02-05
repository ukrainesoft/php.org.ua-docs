---
navigation:
  - function.ssh2-poll.md: « ssh2\_poll
  - function.ssh2-publickey-init.md: ssh2\_publickey\_init »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_publickey\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_publickey\_add

(PECL ssh2 >= 0.10)

ssh2\_publickey\_add — Додає авторизований відкритий ключ

### Опис

```methodsynopsis
ssh2_publickey_add(    resource $pkey,    string $algoname,    string $blob,    bool $overwrite = false,    array $attributes = ?): bool
```

> **Зауваження**: Через підсистему відкритих ключів керують відкритими ключами на сервері, на якому клієнт *вже* пройшов аутентифікацію. Натомість для аутентифікації з відкритим ключем на віддаленій системі викликають функцію [ssh2\_auth\_pubkey\_file()](function.ssh2-auth-pubkey-file.md)

### Список параметрів

`pkey`

Ресурс підсистеми відкритого ключа, створений за допомогою [ssh2\_publickey\_init()](function.ssh2-publickey-init.md)

`algoname`

Алгоритм ключа: ssh-dss, ssh-rsa

`blob`

Бінарний рядок, який містить відкритий ключ

`overwrite`

Чи потрібно перезаписати ключ, якщо він є?

`attributes`

Асоціативний масив атрибутів, які надаються відкритому ключу. Список атрибутів, що підтримуються, шукайте за словами "ietf-secsh-publickey-subsystem". Щоб вказати будь-який атрибут обов'язковим, поставте перед ім'ям зірочку. Якщо сервер не підтримує будь-який атрибут, позначений обов'язковим, це перерве процес додавання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Додаємо відкритий ключ за допомогою **ssh2\_publickey\_add()****

```php
<?php
$ssh2 = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($ssh2, 'jdoe', 'password');
$pkey = ssh2_publickey_init($ssh2);

$keyblob = base64_decode('
AAAAB3NzaC1yc2EAAAABIwAAAIEA5HVt6VqSGd5PTrLRdjNONxXH1tVFGn0
Bd26BF0aCP9qyJRlvdJ3j4WBeX4ZmrveGrjMgkseSYc4xZ26sDHwfL351xj
zaLpipu\BGRrw17mWVBhuCExo476ri5tQFzbTc54VEHYckxQ16CjSTibI5X
69GmnYC9PNqEYq/1TP+HF10=');

ssh2_publickey_add($pkey, 'ssh-rsa', $keyblob, false, array('comment'=>"John's Key"));
?>
```

### Дивіться також

-   [ssh2\_publickey\_init()](function.ssh2-publickey-init.md) \- Ініціалізує підсистему відкритого ключа
-   [ssh2\_publickey\_remove()](function.ssh2-publickey-remove.md) \- Видаляє авторизований відкритий ключ
-   [ssh2\_publickey\_list()](function.ssh2-publickey-list.md) \- Список вже авторизованих відкритих ключів
