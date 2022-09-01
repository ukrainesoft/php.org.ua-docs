---
navigation:
  - function.posix-getuid.html: « posixgetuid
  - function.posix-isatty.html: posixisatty »
  - index.html: PHP Manual
  - ref.posix.html: POSIX Функции
title: posixinitgroups
---
# posixinitgroups

(PHP 5> = 5.2.0, PHP 7, PHP 8)

posixinitgroups — Визначає рівень доступу для групи

### Опис

```methodsynopsis
posix_initgroups(string $username, int $group_id): bool
```

Визначає рівень доступу групи користувача, зазначеного у параметрах.

### Список параметрів

`username`

Ім'я користувача, якого визначається рівень доступу.

`group_id`

Ідентифікатор базової групи із файлу password.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   Керівництво Unix initgroups(3).
