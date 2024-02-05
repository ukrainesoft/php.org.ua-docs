---
navigation:
  - function.posix-getgid.md: « posix\_getgid
  - function.posix-getgrnam.md: posix\_getgrnam »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getgrgid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getgrgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getgrgid — Повертає інформацію про групу за її ID

### Опис

```methodsynopsis
posix_getgrgid(int $group_id): array|false
```

Повертає інформацію про групу за допомогою її ID.

### Список параметрів

`group_id`

Ідентифікатор групи.

### Значення, що повертаються

Масив із наступними елементами:

**Масив з інформацією про групу**

| Элемент | Опис |
| --- | --- |
| name | Елемент name містить назву групи. Це короткий, зазвичай менше 16 символів "дескриптор" групи, що не є повним ім'ям групи. |
| passwd | Елемент passwd містить пароль групи у зашифрованому вигляді. Часто, наприклад, у системах, що використовують "shadow" файли для зберігання інформації про паролі, це поле містить рядок зі зірочок. |
| gid | Елемент містить ID групи та повинен відповідати `group_id` параметру, який використовується під час виклику функції. Цей елемент є надлишковим. |
| members | Цей елемент складається з array, що містить string. Значеннями даного масиву є імена членів цієї групи. |

Функція повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**posix\_getgrgid()\*\*\*\*

```php
<?php

$groupid   = posix_getegid();
$groupinfo = posix_getgrgid($groupid);

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
-   [posix\_getgrnam()](function.posix-getgrnam.md) \- Повертає інформацію про групу, використовуючи її ім'я
-   [filegroup()](function.filegroup.md) \- Отримує ідентифікатор групи файлу
-   [stat()](function.stat.md) \- Повертає інформацію про файл
-   POSIX керівництво GETGRNAM(3)
