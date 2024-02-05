---
navigation:
  - function.ibase-db-info.md: « ibase\_db\_info
  - function.ibase-drop-db.md: ibase\_drop\_db »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_delete\_user
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_delete\_user

(PHP 5, PHP 7 < 7.4.0)

ibase\_delete\_user — Видалення користувача з безпечної бази даних

### Опис

```methodsynopsis
ibase_delete_user(resource $service_handle, string $user_name): bool
```

### Список параметрів

`service_handle`

Дескриптор служби сервера бази даних.

`user_name`

Ім'я користувача, якого потрібно видалити з бази даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_add\_user()](function.ibase-add-user.md) \- Додає користувача до безпечної бази даних
-   [ibase\_modify\_user()](function.ibase-modify-user.md) \- Змінює користувача у безпечній базі даних
