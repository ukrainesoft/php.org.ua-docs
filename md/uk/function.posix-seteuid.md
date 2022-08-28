Встановлює ефективний ідентифікатор користувача для поточного процесу EUID

-   [« posix\_setegid](function.posix-setegid.html)
    
-   [posix\_setgid »](function.posix-setgid.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Встановлює ефективний ідентифікатор користувача для поточного процесу EUID
    

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

-   [posix\_geteuid()](function.posix-geteuid.html) - Повертає ефективний ідентифікатор користувача поточного процесу EUID
-   [posix\_setuid()](function.posix-setuid.html) - Встановлює UID поточного процесу
-   [posix\_getuid()](function.posix-getuid.html) - Повертає фактичний ідентифікатор користувача поточного процесу UID