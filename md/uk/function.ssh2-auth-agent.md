Аутентифікація через SSH за допомогою агента ssh

-   [« Функції SSH2](ref.ssh2.html)
    
-   [ssh2authhostbasedfile »](function.ssh2-auth-hostbased-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SSH2](ref.ssh2.html)
    
-   Аутентифікація через SSH за допомогою агента ssh
    

# ssh2authagent

(PECL ssh2> = 0.12)

ssh2authagent — Аутентифікація через SSH за допомогою агента ssh

### Опис

```methodsynopsis
ssh2_auth_agent(resource $session, string $username): bool
```

Аутентифікація через SSH за допомогою ssh.

> **Зауваження**: Функція **ssh2authagent()** доступна, лише якщо модуль зібраний із бібліотекою libssh >= 1.2.3.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2connect()](function.ssh2-connect.html)

`username`

Ім'я користувача на віддаленому сервері.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Аутентифікація за допомогою агента ssh**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);

if (ssh2_auth_agent($connection, 'username')) {
  echo "Успешная аутентификация !\n";
} else {
  die('Неудачная аутентификация...');
}
?>
```