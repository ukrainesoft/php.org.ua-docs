---
navigation:
  - function.posix-setegid.html: « posixsetegid
  - function.posix-setgid.html: posixsetgid »
  - index.html: PHP Manual
  - ref.posix.html: POSIX Функции
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

-   [posixgeteuid()](function.posix-geteuid.html) - Повертає ефективний ідентифікатор користувача поточного процесу EUID
-   [posixsetuid()](function.posix-setuid.html) - Встановлює UID поточного процесу
-   [posixgetuid()](function.posix-getuid.html) - Повертає фактичний ідентифікатор користувача поточного процесу UID
