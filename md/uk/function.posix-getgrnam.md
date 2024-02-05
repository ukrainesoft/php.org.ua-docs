---
navigation:
  - function.posix-getgrgid.md: « posix\_getgrgid
  - function.posix-getgroups.md: posix\_getgroups »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getgrnam
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getgrnam

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getgrnam — Повертає інформацію про групу, використовуючи її ім'я

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

| Элемент | Опис |
| --- | --- |
| name | Елемент name містить назву групи. Це короткий, зазвичай менше 16 символів "дескриптор" групи, що не є дійсним повним ім'ям групи. Він має відповідати `name` параметра, що використовується в цій функції. Елемент є надлишковим. |
| passwd | Елемент passwd містить пароль групи у зашифрованому вигляді. Часто, наприклад, у системах, що використовують "shadow" файли для зберігання інформації про паролі, це поле містить зірочку. |
| gid | Ідентифікатор групи, що складається із цифр. |
| members | Цей елемент складається з array, що містить string. Значеннями даного масиву є імена членів цієї групи. |

### Приклади

**Приклад #1 Приклад використання** posix\_getgrnam()\*\*\*\*

```php
<?php

$groupinfo = posix_getgrnam("toons");

print_r($groupinfo);
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [posix\_getegid()](function.posix-getegid.md) \- Повертає ефективний ідентифікатор групи поточного процесу EGID
-   [posix\_getgrgid()](function.posix-getgrgid.md) \- Повертає інформацію про групу за її ID
-   [filegroup()](function.filegroup.md) \- Отримує ідентифікатор групи файлу
-   [stat()](function.stat.md) \- Повертає інформацію про файл
-   POSIX керівництво GETGRNAM(3)
