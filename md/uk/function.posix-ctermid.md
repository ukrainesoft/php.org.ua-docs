---
navigation:
  - function.posix-access.md: « posixaccess
  - function.posix-errno.md: posixerrno »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixctermid
---
# posixctermid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixctermid - Повертає шлях керуючого терміналу

### Опис

```methodsynopsis
posix_ctermid(): string|false
```

Повертає змінну типу string, що містить шлях до поточного керуючого терміналу цього процесу. У разі виникнення помилки буде встановлено її номер, який можна обробити з використанням [posixgetlasterror()](function.posix-get-last-error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає string шляхом до поточного керуючого терміналу. В іншому випадку повертає **`false`** та встановлює номер помилки, який може бути оброблений за допомогою [posixgetlasterror()](function.posix-get-last-error.md)

### Приклади

**Приклад #1 Приклад використання **posixctermid()****

Цей скрипт виводить шлях до поточного керуючого терміналу (TTY).

```php
<?php
echo "I am running from ".posix_ctermid();
?>
```

### Дивіться також

-   [posixttyname()](function.posix-ttyname.md) - Визначає ім'я термінального пристрою
-   [posixgetlasterror()](function.posix-get-last-error.md) - Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею
