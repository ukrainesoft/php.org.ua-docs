---
navigation:
  - function.posix-setegid.md: « posix\_setegid
  - function.posix-setgid.md: posix\_setgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_seteuid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_seteuid

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

posix\_seteuid — Встановлює ефективний ідентифікатор користувача для поточного процесу EUID

### Опис

```methodsynopsis
posix_seteuid(int $user_id): bool
```

Встановлює ефективний ідентифікатор користувача. Це привілейована функція і вимагає відповідних прав (як правило, прав суперкористувача root) щоб мати можливість виконати її.

### Список параметрів

`user_id`

Ідентифікатор користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [posix\_geteuid()](function.posix-geteuid.md) \- Повертає ефективний ідентифікатор користувача поточного процесу EUID
-   [posix\_setuid()](function.posix-setuid.md) \- Встановлює UID поточного процесу
-   [posix\_getuid()](function.posix-getuid.md) \- Повертає фактичний ідентифікатор користувача поточного процесу UID
