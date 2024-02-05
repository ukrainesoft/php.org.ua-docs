---
navigation:
  - function.ssh2-publickey-add.md: « ssh2\_publickey\_add
  - function.ssh2-publickey-list.md: ssh2\_publickey\_list »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_publickey\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_publickey\_init

(PECL ssh2 >= 0.10)

ssh2\_publickey\_init - Ініціалізує підсистему відкритого ключа

### Опис

```methodsynopsis
ssh2_publickey_init(resource $session): resource|false
```

Запитує підсистему відкритого ключа із вже відкритого з'єднання SSH2.

Підсистема відкритого ключа дозволяє авторизованому клієнту керувати списком авторизованих відкритих ключів, що зберігаються на сервері незалежно. Якщо віддалений сервер не підтримує підсистему відкритого ключа, функція **ssh2\_publickey\_init()** поверне **`false`**

### Список параметрів

`session`

### Значення, що повертаються

Повертає ресурс `підсистеми відкритого ключа SSH2` (SSH2 Publickey Subsystem) для використання з іншими методами ssh2\_publickey\_\*() или\*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження**: Через підсистему відкритих ключів керують відкритими ключами на сервері, на якому клієнт *вже* пройшов аутентифікацію. Натомість для аутентифікації з відкритим ключем на віддаленій системі викликають функцію [ssh2\_auth\_pubkey\_file()](function.ssh2-auth-pubkey-file.md)

### Дивіться також

-   [ssh2\_publickey\_add()](function.ssh2-publickey-add.md) \- Додає авторизований відкритий ключ
-   [ssh2\_publickey\_remove()](function.ssh2-publickey-remove.md) \- Видаляє авторизований відкритий ключ
-   [ssh2\_publickey\_list()](function.ssh2-publickey-list.md) \- Список вже авторизованих відкритих ключів
