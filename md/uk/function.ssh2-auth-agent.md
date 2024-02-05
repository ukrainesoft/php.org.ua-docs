---
navigation:
  - ref.ssh2.md: « Функції SSH2
  - function.ssh2-auth-hostbased-file.md: ssh2\_auth\_hostbased\_file »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_auth\_agent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_auth\_agent

(PECL ssh2 >= 0.12)

ssh2\_auth\_agent — Аутентифікація через SSH за допомогою агента ssh

### Опис

```methodsynopsis
ssh2_auth_agent(resource $session, string $username): bool
```

Аутентифікація через SSH за допомогою ssh.

> **Зауваження**: Функция**ssh2\_auth\_agent()** доступна, лише якщо модуль зібраний із бібліотекою libssh >= 1.2.3.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`username`

Ім'я користувача на віддаленому сервері.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Аутентифікація за допомогою агента ssh**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);

if (ssh2_auth_agent($connection, 'username')) {
  echo "Успешная аутентификация !\n";
} else {
  die('Неудачная аутентификация...');
}
?>
```
