---
navigation:
  - function.ssh2-publickey-list.html: « ssh2publickeylist
  - function.ssh2-scp-recv.html: ssh2scprecv »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2publickeyremove
---
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

> **Зауваження**: Підсистема відкритих ключів використовується для керування відкритими ключами на сервері, на якому клієнт *вже* пройшов авторизацію. Для авторизації за допомогою відкритого ключа на віддаленій системі, використовуйте натомість функцію [ssh2authpubkeyfile()](function.ssh2-auth-pubkey-file.md)

### Дивіться також

-   [ssh2publickeyinit()](function.ssh2-publickey-init.md) - Ініціалізує підсистему відкритого ключа
-   [ssh2publickeyadd()](function.ssh2-publickey-add.md) - Додає авторизований відкритий ключ
-   [ssh2publickeylist()](function.ssh2-publickey-list.md) - Список вже авторизованих відкритих ключів
