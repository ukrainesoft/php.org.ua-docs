Встановлює ідентифікатор групи для поточного процесу GID

-   [« posix\_seteuid](function.posix-seteuid.html)
    
-   [posix\_setpgid »](function.posix-setpgid.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Встановлює ідентифікатор групи для поточного процесу GID
    

# posixsetgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixsetgid - Встановлює ідентифікатор групи для поточного процесу GID

### Опис

```methodsynopsis
posix_setgid(int $group_id): bool
```

Визначає фактичний ідентифікатор групи поточного процесу. Це привілейована функція і потребує відповідних прав (зазвичай прав суперкористувача root) у системі, щоб мати можливість виконати її. Правильним є такий порядок виклику функцій: спочатку **posixsetgid()**, потім [posix\_setuid()](function.posix-setuid.html)

> **Зауваження**
> 
> Якщо функція буде викликана суперкористувачем, то також буде встановлений ефективний ідентифікатор групи користувача.

### Список параметрів

`group_id`

Ідентифікатор групи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **posixsetgid()****

Код нижче виводить ефективний ідентифікатор групи до та після зміни.

```php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setgid(40);
echo 'My real group id is '.posix_getgid(); //40
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Дивіться також

-   [posix\_getgrgid()](function.posix-getgrgid.html) - Повертає інформацію про групу за її ID
-   [posix\_getgid()](function.posix-getgid.html) - Повертає дійсний ID групи поточного процесу GID