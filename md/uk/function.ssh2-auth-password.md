Аутентифікація через SSH з використанням звичайного пароля

-   [« ssh2\_auth\_none](function.ssh2-auth-none.html)
    
-   [ssh2\_auth\_pubkey\_file »](function.ssh2-auth-pubkey-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Аутентифікація через SSH з використанням звичайного пароля
    

# ssh2authpassword

(PECL ssh2> = 0.9.0)

ssh2authpassword — Аутентифікація через SSH за допомогою звичайного пароля

### Опис

```methodsynopsis
ssh2_auth_password(resource $session, string $username, string $password): bool
```

Аутентифікація через SSH за допомогою звичайного пароля. Починаючи з версії 0.12, ця функція також підтримує запит пароля з клавіатури.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.html)

`username`

Ім'я користувача на віддаленому сервері.

`password`

Пароль для `username`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Аутентифікація з паролем**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);

if (ssh2_auth_password($connection, 'username', 'secret')) {
  echo "Успешная аутентификация!\n";
} else {
  die('Неудачная аутентификация...');
}
?>
```