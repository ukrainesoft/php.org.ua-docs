Повертає шлях керуючого терміналу

-   [« posix\_access](function.posix-access.html)
    
-   [posix\_errno »](function.posix-errno.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Повертає шлях керуючого терміналу
    

# posixctermid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixctermid - Повертає шлях керуючого терміналу

### Опис

```methodsynopsis
posix_ctermid(): string|false
```

Повертає змінну типу string, що містить шлях до поточного керуючого терміналу цього процесу. У разі виникнення помилки буде встановлено її номер, який можна обробити з використанням [posix\_get\_last\_error()](function.posix-get-last-error.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає string шляхом до поточного керуючого терміналу. В іншому випадку повертає **`false`** та встановлює номер помилки, який може бути оброблений за допомогою [posix\_get\_last\_error()](function.posix-get-last-error.html)

### Приклади

**Приклад #1 Приклад використання **posixctermid()****

Цей скрипт виводить шлях до поточного керуючого терміналу (TTY).

```php
<?php
echo "I am running from ".posix_ctermid();
?>
```

### Дивіться також

-   [posix\_ttyname()](function.posix-ttyname.html) - Визначає ім'я термінального пристрою
-   [posix\_get\_last\_error()](function.posix-get-last-error.html) - Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею