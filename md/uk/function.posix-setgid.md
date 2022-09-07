---
navigation:
  - function.posix-seteuid.md: « posixseteuid
  - function.posix-setpgid.md: posixsetpgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixsetgid
---
# posixsetgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixsetgid - Встановлює ідентифікатор групи для поточного процесу GID

### Опис

```methodsynopsis
posix_setgid(int $group_id): bool
```

Визначає фактичний ідентифікатор групи поточного процесу. Це привілейована функція і потребує відповідних прав (зазвичай прав суперкористувача root) у системі, щоб мати можливість виконати її. Правильним є такий порядок виклику функцій: спочатку **posixsetgid()**, потім [posixsetuid()](function.posix-setuid.md)

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
echo 'My real group id is '.posix_getgid(); //20
posix_setgid(40);
echo 'My real group id is '.posix_getgid(); //40
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Дивіться також

-   [posixgetgrgid()](function.posix-getgrgid.md) - Повертає інформацію про групу за її ID
-   [posixgetgid()](function.posix-getgid.md) - Повертає дійсний ID групи поточного процесу GID
