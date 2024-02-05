---
navigation:
  - function.ibase-maintain-db.md: « ibase\_maintain\_db
  - function.ibase-name-result.md: ibase\_name\_result »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_modify\_user
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_modify\_user

(PHP 5, PHP 7 < 7.4.0)

ibase\_modify\_user — Змінює користувача у безпечній базі даних

### Опис

```methodsynopsis
ibase_modify_user(    resource $service_handle,    string $user_name,    string $password,    string $first_name = ?,    string $middle_name = ?,    string $last_name = ?): bool
```

### Список параметрів

`service_handle`

Дескриптор служби сервера бази даних.

`user_name`

Ім'я користувача бази даних для зміни.

`password`

Новий пароль користувача.

`first_name`

Нове ім'я користувача.

`middle_name`

Нове по батькові користувача.

`last_name`

Нове прізвище користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_add\_user()](function.ibase-add-user.md) \- Додає користувача до безпечної бази даних
-   [ibase\_delete\_user()](function.ibase-delete-user.md) \- Видаляє користувача з безпечної бази даних
