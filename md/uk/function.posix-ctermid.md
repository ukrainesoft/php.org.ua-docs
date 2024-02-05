---
navigation:
  - function.posix-access.md: « posix\_access
  - function.posix-eaccess.md: posix\_eaccess »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_ctermid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_ctermid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_ctermid - Повертає шлях керуючого терміналу

### Опис

```methodsynopsis
posix_ctermid(): string|false
```

Повертає змінну типу string, що містить шлях до поточного керуючого терміналу цього процесу. У разі виникнення помилки буде встановлено її номер, який можна обробити з використанням [posix\_get\_last\_error()](function.posix-get-last-error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає string шляхом до поточного керуючого терміналу. В іншому випадку повертає **`false`** та встановлює номер помилки, який може бути оброблений за допомогою [posix\_get\_last\_error()](function.posix-get-last-error.md)

### Приклади

**Приклад #1 Приклад використання** posix\_ctermid()\*\*\*\*

Цей скрипт виводить шлях до поточного керуючого терміналу (TTY).

```php
<?php
echo "I am running from ".posix_ctermid();
?>
```

### Дивіться також

-   [posix\_ttyname()](function.posix-ttyname.md) \- Визначає ім'я термінального пристрою
-   [posix\_get\_last\_error()](function.posix-get-last-error.md) \- Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею
