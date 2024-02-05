---
navigation:
  - function.posix-pathconf.md: « posix\_pathconf
  - function.posix-seteuid.md: posix\_seteuid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_setegid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_setegid

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

posix\_setegid — Встановлює ефективний ідентифікатор групи для поточного процесу EGID

### Опис

```methodsynopsis
posix_setegid(int $group_id): bool
```

Встановлює ефективний ідентифікатор групи для поточного процесу. Це привілейована функція і вимагає відповідних прав (як правило, прав суперкористувача root) в системі, щоб мати можливість виконувати її.

### Список параметрів

`group_id`

Ефективний ідентифікатор групи, що встановлюється, для поточного процесу

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**posix\_setegid()\*\*\*\*

Цей приклад виводить ефективний ідентифікатор групи процесу до та після зміни.

```php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Дивіться також

-   [posix\_getgrgid()](function.posix-getgrgid.md) \- Повертає інформацію про групу за її ID
-   [posix\_getgid()](function.posix-getgid.md) \- Повертає дійсний ID групи поточного процесу GID
-   [posix\_setgid()](function.posix-setgid.md) \- Встановлює ідентифікатор групи для поточного процесу GID
