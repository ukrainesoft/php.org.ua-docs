Список вже авторизованих відкритих ключів

-   [« ssh2\_publickey\_init](function.ssh2-publickey-init.html)
    
-   [ssh2\_publickey\_remove »](function.ssh2-publickey-remove.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Список вже авторизованих відкритих ключів
    

# ssh2publickeylist

(PECL ssh2> = 0.10)

ssh2publickeylist - Список вже авторизованих відкритих ключів

### Опис

```methodsynopsis
ssh2_publickey_list(resource $pkey): array
```

Список нині авторизованих відкритих ключів.

### Список параметрів

`pkey`

Ресурс підсистеми відкритого ключа

### Значення, що повертаються

Повертає індексований масив ключів, кожен з яких є асоціативним масивом, що містить елементи з ключами: name, blob, attrs.

**Елементи публічного ключа**

| Ключ массива | Что означает                                                                                                                                                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name         | Ім'я алгоритму, за допомогою якого створювався ключ: `ssh-dss` або `ssh-rsa`                                                                                                |
| blob         | Рядок бінарних даних - сам ключ                                                                                                                                             |
| attrs        | Атрибути, надані ключу. Найчастіше використовується (і єдиний доступний підсистемою відкритого ключа версії 1) - це `comment`, Що представляє собою рядок вільного формату. |

### Приклади

**Приклад #1 Список авторизованих ключів за допомогою **ssh2publickeylist()****

```php
<?php
$ssh2 = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($ssh2, 'jdoe', 'secret');
$pkey = ssh2_publickey_init($ssh2);

$list = ssh2_publickey_list($pkey);

foreach($list as $key) {
  echo "Key: {$key['name']}\n";
  echo "Blob: " . chunk_split(base64_encode($key['blob']), 40, "\n") . "\n";
  echo "Comment: {$key['attrs']['comment']}\n\n";
}
?>
```

Результат виконання цього прикладу:

```
Key: ssh-rsa
Blob: AAAAB3NzaC1yc2EAAAABIwAAAIEA5HVt6VqSGd5P
TrLRdjNONxXH1tVFGn0Bd26BF0aCP9qyJRlvdJ3j
4WBeX4ZmrveGrjMgkseSYc4xZ26sDHwfL351xjza
Lpipu\BGRrw17mWVBhuCExo476ri5tQFzbTc54VE
HYckxQ16CjSTibI5X69GmnYC9PNqEYq/1TP+HF10
Comment: John's Key

Key: ssh-rsa
Blob: AAAAB3NzaHVt6VqSGd5C1yc2EAAAABIwA232dnJA
AIEA5HVt6VqSGd5PTrLRdjNONxX/1TP+HF1HVt6V
qSGd50H1tVFGn0BB3NzaC1yc2EAd26BF0aCP9qyJ
RlvdJ3j4WBeX4ZmrveGrjMgkseSYc4xZ26HVt6Vq
SGd5sDHwfL351xjzaLpipu\BGB3NzaC1yc2EA/1T
Comment: Alice's Key
```

### Примітки

> **Зауваження**: Підсистема відкритих ключів використовується для керування відкритими ключами на сервері, на якому клієнт *вже* пройшов авторизацію. Для авторизації за допомогою відкритого ключа на віддаленій системі, використовуйте натомість функцію [ssh2\_auth\_pubkey\_file()](function.ssh2-auth-pubkey-file.html)

### Дивіться також

-   [ssh2\_publickey\_init()](function.ssh2-publickey-init.html) - Ініціалізує підсистему відкритого ключа
-   [ssh2\_publickey\_add()](function.ssh2-publickey-add.html) - Додає авторизований відкритий ключ
-   [ssh2\_publickey\_remove()](function.ssh2-publickey-remove.html) - Видаляє авторизований відкритий ключ