Змінює користувача у безпечній базі даних

-   [« ibasemaintainдб](function.ibase-maintain-db.html)
    
-   [ibasenameresult »](function.ibase-name-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Змінює користувача у безпечній базі даних
    

# ibasemodifyuser

(PHP 5, PHP 7 < 7.4.0)

ibasemodifyuser — Змінює користувача у безпечній базі даних

### Опис

```methodsynopsis
ibase_modify_user(    resource $service_handle,    string $user_name,    string $password,    string $first_name = ?,    string $middle_name = ?,    string $last_name = ?): bool
```

### Список параметрів

`service_handle`

Дескриптор служби сервера бази даних.

`user_name`

Ім'я користувача бази даних зміни.

`password`

Новий пароль користувача.

`first_name`

Нове ім'я користувача.

`middle_name`

Нове по батькові користувача.

`last_name`

Нове прізвище користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseadduser()](function.ibase-add-user.html) - Додає користувача до безпечної бази даних
-   [ibasedeleteuser()](function.ibase-delete-user.html) - Видаляє користувача з безпечної бази даних