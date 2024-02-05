---
navigation:
  - function.ssh2-auth-none.md: « ssh2\_auth\_none
  - function.ssh2-auth-pubkey-file.md: ssh2\_auth\_pubkey\_file »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_auth\_password
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_auth\_password

(PECL ssh2 >= 0.9.0)

ssh2\_auth\_password — Аутентифікація через SSH за допомогою звичайного пароля

### Опис

```methodsynopsis
ssh2_auth_password(resource $session, string $username, string $password): bool
```

Аутентифікація через SSH за допомогою звичайного пароля. Починаючи з версії 0.12, ця функція також підтримує запит пароля з клавіатури.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`username`

Ім'я користувача на віддаленому сервері.

`password`

Пароль для`username`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Аутентифікація з паролем**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);

if (ssh2_auth_password($connection, 'username', 'secret')) {
  echo "Успешная аутентификация!\n";
} else {
  die('Неудачная аутентификация...');
}
?>
```
