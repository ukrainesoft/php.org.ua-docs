---
navigation:
  - function.ssh2-auth-hostbased-file.md: « ssh2authhostbasedfile
  - function.ssh2-auth-password.md: ssh2authpassword »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2authnone
---
# ssh2authnone

(PECL ssh2> = 0.9.0)

ssh2authnone - Аутентифікація як "none"

### Опис

```methodsynopsis
ssh2_auth_none(resource $session, string $username): mixed
```

Спроба пройти аутентифікацію як "none" зазвичай буде зазнавати невдачі (і має). Разом з помилкою ця функція поверне список доступних методів автентифікації.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2connect()](function.ssh2-connect.md)

`username`

Ім'я користувача на віддаленому сервері.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо сервер приймає аутентифікацію "none", або масив доступних методів аутентифікації.

### Приклади

**Приклад #1 Вилучення списку доступних методів автентифікації**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);

$auth_methods = ssh2_auth_none($connection, 'user');

if (in_array('password', $auth_methods)) {
  echo "Сервер поддерживает аутентификацию на основе пароля\n";
}
?>
```
