Змінює пароль користувача Oracle

-   [« ociparse](function.oci-parse.html)
    
-   [ocipconnect »](function.oci-pconnect.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Змінює пароль користувача Oracle
    

# ocipasswordchange

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocipasswordchange — Змінює пароль користувача Oracle

### Опис

```methodsynopsis
oci_password_change(    resource $connection,    string $username,    string $old_password,    string $new_password): bool
```

```methodsynopsis
oci_password_change(    string $database_name,    string $username,    string $old_password,    string $new_password): resource
```

Змінює пароль користувача, вказаного в `username`

Функція **ocipasswordchange()** особливо корисна для скриптів PHP командного рядка або під час використання непостійних з'єднань у всьому додатку PHP.

### Список параметрів

`connection`

Ідентифікатор з'єднання, що повертається функцією [ociconnect()](function.oci-connect.html) або [ocipconnect()](function.oci-pconnect.html)

`username`

Ім'я користувача Oracle.

`old_password`

Старий пароль.

`new_password`

Новий пароль.

`database_name`

Назва бази даних.

### Значення, що повертаються

Якщо вказано параметр `connection` **ocipasswordchange()** повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо вказано параметр `connection` **ocipasswordchange()** повертає ресурс з'єднання у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ocipasswordchange()** зі зміною пароля вже підключеного користувача**

```php
<?php

$dbase      = 'localhost/orcl';
$user       = 'cj';
$current_pw = 'welcome';
$new_pw     = 'geelong';

$c = oci_pconnect($user, $current_pw, $dbase);
oci_password_change($c, $user, $current_pw, $new_pw);
echo "Новый пароль : " . $new_pw . "\n";

?>
```

**Приклад #2 Приклад використання **ocipasswordchange()** із підключенням та зміною пароля одночасно**

```php
<?php

$dbase      = 'localhost/orcl';
$user       = 'cj';
$current_pw = 'welcome';
$new_pw     = 'geelong';

$c = oci_pconnect($user, $current_pw, $dbase);
if (!$c) {
    $m = oci_error();
    if ($m['code'] == 28001) { // "ORA-28001: the password has expired"
        // Подключение и сброс пароля одновременно
        $c = oci_password_change($dbase, $user, $current_pw, $new_pw);
        if ($c) {
            echo "Новый пароль : " . $new_pw . "\n";
        }
    }
}

if (!$c) {  // Ошибка не совпадала с 28001, или не получилось изменить пароль
    $m = oci_error();
    trigger_error('Не удалось подключиться к базе данных: '. $m['message'], E_USER_ERROR);
}

// Использование подключения $c
// ...

?>
```

### Примітки

> **Зауваження**
> 
> Зміна пароля за допомогою цієї функції або безпосередньо в Oracle має виконуватися акуратно, оскільки PHP-додаток може продовжувати використовувати в постійних з'єднаннях дані автентифікації останнього успішного підключення, які вже застаріли. Найкращим рішенням може бути перезапуск усіх веб-серверів після зміни пароля.

> **Зауваження**
> 
> При оновленні бібліотеки клієнта Oracle або бази даних від версії установки до версії 11.2.0.3 та вище функція **ocipasswordchange()** може повернути помилку "ORA-1017: invalid username/password" (Невірні ім'я користувача/пароль), якщо версії клієнта та сервера оновлені в один час.

> **Зауваження**
> 
> Другий набір параметрів функції **ocipasswordchange()** доступний, починаючи з версії OCI8 1.1.

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася **ocipasswordchange()**. У PHP 5.0.0 і вище **ocipasswordchange()** є аліасом **ocipasswordchange()** для зворотної сумісності, ви можете продовжувати використовувати це ім'я, але це не рекомендується.