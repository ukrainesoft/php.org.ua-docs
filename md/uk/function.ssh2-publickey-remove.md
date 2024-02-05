---
navigation:
  - function.ssh2-publickey-list.md: « ssh2\_publickey\_list
  - function.ssh2-scp-recv.md: ssh2\_scp\_recv »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_publickey\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_publickey\_remove

(PECL ssh2 >= 0.10)

ssh2\_publickey\_remove — Видаляє авторизований відкритий ключ

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження**: Через підсистему відкритих ключів керують відкритими ключами на сервері, на якому клієнт *вже* пройшов аутентифікацію. Натомість для аутентифікації з відкритим ключем на віддаленій системі викликають функцію [ssh2\_auth\_pubkey\_file()](function.ssh2-auth-pubkey-file.md)

### Дивіться також

-   [ssh2\_publickey\_init()](function.ssh2-publickey-init.md) \- Ініціалізує підсистему відкритого ключа
-   [ssh2\_publickey\_add()](function.ssh2-publickey-add.md) \- Додає авторизований відкритий ключ
-   [ssh2\_publickey\_list()](function.ssh2-publickey-list.md) \- Список вже авторизованих відкритих ключів
