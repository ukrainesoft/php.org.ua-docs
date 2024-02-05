---
navigation:
  - function.fbird-wait-event.md: « fbird\_wait\_event
  - function.ibase-affected-rows.md: ibase\_affected\_rows »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_add\_user
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_add\_user

(PHP 5, PHP 7 < 7.4.0)

ibase\_add\_user — Додає користувача до безпечної бази даних

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_modify\_user()](function.ibase-modify-user.md) \- Змінює користувача у безпечній базі даних
-   [ibase\_delete\_user()](function.ibase-delete-user.md) \- Видаляє користувача з безпечної бази даних
