---
navigation:
  - function.posix-setegid.md: « posixsetegid
  - function.posix-setgid.md: posixsetgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixseteuid
---
# posixseteuid

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

posixseteuid — Встановлює ефективний ідентифікатор користувача для поточного процесу EUID

### Опис

```methodsynopsis
posix_seteuid(int $user_id): bool
```

Встановлює ефективний ідентифікатор користувача. Це привілейована функція і вимагає відповідних прав (як правило, прав суперкористувача root) щоб мати можливість виконати її.

### Список параметрів

`user_id`

Ідентифікатор користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [posixgeteuid()](function.posix-geteuid.md) - Повертає ефективний ідентифікатор користувача поточного процесу EUID
-   [posixsetuid()](function.posix-setuid.md) - Встановлює UID поточного процесу
-   [posixgetuid()](function.posix-getuid.md) - Повертає фактичний ідентифікатор користувача поточного процесу UID
