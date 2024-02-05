---
navigation:
  - function.posix-fpathconf.md: « posix\_fpathconf
  - function.posix-getcwd.md: posix\_getcwd »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_get\_last\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_get\_last\_error

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

posix\_get\_last\_error — Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею

### Опис

```methodsynopsis
posix_get_last_error(): int
```

Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею. Системне повідомлення про помилку, яке відповідає її номеру, може бути отримане за допомогою [posix\_strerror()](function.posix-strerror.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер помилки, встановлений останньою posix функцією, що завершилася невдачею. У разі відсутності помилок повертає 0.

### Приклади

**Приклад #1 Приклад використання** posix\_get\_last\_error()\*\*\*\*

У цьому прикладі відбувається спроба завершити неіснуючий процес з його id. Спроба завершується невдачею та повертає номер помилки, який буде виведено.

```php
<?php
posix_kill(999459,SIGKILL);
echo 'Your error returned was '.posix_get_last_error(); //Your error was ___
?>
```

### Дивіться також

-   [posix\_strerror()](function.posix-strerror.md) \- Повертає системне повідомлення про помилку, ґрунтуючись на отриманому номері помилки
