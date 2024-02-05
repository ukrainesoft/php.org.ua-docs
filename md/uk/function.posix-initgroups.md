---
navigation:
  - function.posix-getuid.md: « posix\_getuid
  - function.posix-isatty.md: posix\_isatty »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_initgroups
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_initgroups

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

posix\_initgroups — Визначає рівень доступу для групи

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   Керівництво Unix initgroups(3).
