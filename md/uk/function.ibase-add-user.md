Додає користувача до безпечної бази даних

-   [« fbirdwaitevent](function.fbird-wait-event.html)
    
-   [ibaseaffectedrows »](function.ibase-affected-rows.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Додає користувача до безпечної бази даних
    

# ibaseadduser

(PHP 5, PHP 7 < 7.4.0)

ibaseadduser — Додає користувача до безпечної бази даних

### Опис

```methodsynopsis
ibase_add_user(    resource $service_handle,    string $user_name,    string $password,    string $first_name = ?,    string $middle_name = ?,    string $last_name = ?): bool
```

### Список параметрів

`service_handle`

Дескриптор служби сервера бази даних.

`user_name`

Ім'я для входу нового користувача бази даних.

`password`

Пароль нового користувача.

`first_name`

Ім'я нового користувача бази даних.

`middle_name`

По-батькові нового користувача бази даних.

`last_name`

Прізвище нового користувача бази даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibasemodifyuser()](function.ibase-modify-user.html) - Змінює користувача у безпечній базі даних
-   [ibasedeleteuser()](function.ibase-delete-user.html) - Видаляє користувача з безпечної бази даних