Встановлює ефективний ідентифікатор групи для поточного процесу EGID

-   [« posixmknod](function.posix-mknod.html)
    
-   [posixseteuid »](function.posix-seteuid.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Встановлює ефективний ідентифікатор групи для поточного процесу EGID
    

# posixsetegid

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

posixsetegid — Встановлює ефективний ідентифікатор групи для поточного процесу EGID

### Опис

```methodsynopsis
posix_setegid(int $group_id): bool
```

Встановлює ефективний ідентифікатор групи для поточного процесу. Це привілейована функція і вимагає відповідних прав (як правило, прав суперкористувача root) в системі, щоб мати можливість виконувати її.

### Список параметрів

`group_id`

Ефективний ідентифікатор групи, що встановлюється, для поточного процесу

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **posixsetegid()****

Цей приклад виводить ефективний ідентифікатор групи процесу до та після зміни.

```php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Дивіться також

-   [posixgetgrgid()](function.posix-getgrgid.html) - Повертає інформацію про групу за її ID
-   [posixgetgid()](function.posix-getgid.html) - Повертає дійсний ID групи поточного процесу GID
-   [posixsetgid()](function.posix-setgid.html) - Встановлює ідентифікатор групи для поточного процесу GID