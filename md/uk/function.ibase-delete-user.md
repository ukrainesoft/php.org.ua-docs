---
navigation:
  - function.ibase-db-info.html: « ibaseдбinfo
  - function.ibase-drop-db.html: ibasedropdb »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasedeleteuser
---
# ibasedeleteuser

(PHP 5, PHP 7 < 7.4.0)

ibasedeleteuser — Видалення користувача з безпечної бази даних

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseadduser()](function.ibase-add-user.html) - Додає користувача до безпечної бази даних
-   [ibasemodifyuser()](function.ibase-modify-user.html) - Змінює користувача у безпечній базі даних
