---
navigation:
  - function.posix-get-last-error.md: « posixgetlasterror
  - function.posix-getegid.md: posixgetegid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgetcwd
---
# posixgetcwd

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetcwd — Повертає шлях поточної директорії

### Опис

```methodsynopsis
posix_getcwd(): string|false
```

Повертає абсолютний шлях робочої директорії скрипта. У разі виникнення помилки буде встановлено її номер, який може бути оброблений за допомогою [posixgetlasterror()](function.posix-get-last-error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає string з абсолютним шляхом у разі успішного виконання. У разі виникнення помилки буде повернено **`false`**, також буде встановлено номер помилки, який може бути оброблений за допомогою [posixgetlasterror()](function.posix-get-last-error.md)

### Приклади

**Приклад #1 Приклад використання **posixgetcwd()****

У цьому прикладі повертається абсолютний шлях робочої директорії скрипта, що виконується.

```php
<?php
echo 'My current working directory is '.posix_getcwd();
?>
```

### Примітки

> **Зауваження**
> 
> Функція завершиться помилкою у таких випадках
> 
> -   Відсутні права на читання чи пошук
> -   Даного шляху більше не існує
