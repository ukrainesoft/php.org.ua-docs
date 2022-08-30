Видаляє авторизований відкритий ключ

-   [« ssh2publickeylist](function.ssh2-publickey-list.html)
    
-   [ssh2scprecv »](function.ssh2-scp-recv.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SSH2](ref.ssh2.html)
    
-   Видаляє авторизований відкритий ключ
    

# ssh2publickeyremove

(PECL ssh2> = 0.10)

ssh2publickeyremove — Видаляє авторизований відкритий ключ

### Опис

```methodsynopsis
ssh2_publickey_remove(resource $pkey, string $algoname, string $blob): bool
```

Видаляє авторизований відкритий ключ.

### Список параметрів

`pkey`

Ресурс підсистеми відкритого ключа

`algoname`

Алгоритм ключа: ssh-dss, ssh-rsa

`blob`

Бінарний рядок, що містить ключ

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**: Підсистема відкритих ключів використовується для керування відкритими ключами на сервері, на якому клієнт *вже* пройшов авторизацію. Для авторизації за допомогою відкритого ключа на віддаленій системі, використовуйте натомість функцію [ssh2authpubkeyfile()](function.ssh2-auth-pubkey-file.html)

### Дивіться також

-   [ssh2publickeyinit()](function.ssh2-publickey-init.html) - Ініціалізує підсистему відкритого ключа
-   [ssh2publickeyadd()](function.ssh2-publickey-add.html) - Додає авторизований відкритий ключ
-   [ssh2publickeylist()](function.ssh2-publickey-list.html) - Список вже авторизованих відкритих ключів