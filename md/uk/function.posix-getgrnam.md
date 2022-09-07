---
navigation:
  - function.posix-getgrgid.md: « posixgetgrgid
  - function.posix-getgroups.md: posixgetgroups »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgetgrnam
---
# posixgetgrnam

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetgrnam — Повертає інформацію про групу, використовуючи її ім'я

### Опис

```methodsynopsis
posix_getgrnam(string $name): array|false
```

Повертає інформацію про групу, використовуючи її ім'я.

### Список параметрів

`name`

Ім'я групи

### Значення, що повертаються

Повертає масив (array) у разі успішного виконання або **`false`** у разі виникнення помилки. Повертається масив має такі елементи:

**Масив з інформацією про групу**

| Элемент | Описание |
| --- | --- |
| name | Елемент name містить назву групи. Це короткий, зазвичай менше 16 символів "дескриптор" групи, що не є дійсним повним ім'ям групи. Він має відповідати `name` параметра, що використовується в цій функції. Елемент є надлишковим. |
| passwd | Елемент passwd містить пароль групи у зашифрованому вигляді. Часто, наприклад, у системах, що використовують "shadow" файли для зберігання інформації про паролі, це поле містить зірочку. |
| gid | Ідентифікатор групи, що складається із цифр. |
| members | Цей елемент складається з array, що містить string. Значеннями даного масиву є імена членів цієї групи. |

### Приклади

**Приклад #1 Приклад використання **posixgetgrnam()****

```php
<?php

$groupinfo = posix_getgrnam("toons");

print_r($groupinfo);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [name]    => toons
    [passwd]  => x
    [members] => Array
        (
            [0] => tom
            [1] => jerry
        )
    [gid]     => 42
)
```

### Дивіться також

-   [posixgetegid()](function.posix-getegid.md) - Повертає ефективний ідентифікатор групи поточного процесу EGID
-   [posixgetgrgid()](function.posix-getgrgid.md) - Повертає інформацію про групу за її ID
-   [filegroup()](function.filegroup.md) - Отримує ідентифікатор групи файлу
-   [stat()](function.stat.md) - Повертає інформацію про файл
-   POSIX керівництво GETGRNAM(3)
