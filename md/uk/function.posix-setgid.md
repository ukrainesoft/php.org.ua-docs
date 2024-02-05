---
navigation:
  - function.posix-seteuid.md: « posix\_seteuid
  - function.posix-setpgid.md: posix\_setpgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_setgid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_setgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_setgid - Встановлює ідентифікатор групи для поточного процесу GID

### Опис

```methodsynopsis
posix_setgid(int $group_id): bool
```

Встановлює фактичний ідентифікатор групи поточного процесу. Це привілейована функція і потребує відповідних прав (зазвичай прав суперкористувача root) у системі, щоб мати можливість виконати її. Правильним є такий порядок виклику функцій: спочатку **posix\_setgid()**, потім [posix\_setuid()](function.posix-setuid.md)

> **Зауваження** :
> 
> Якщо функція буде викликана суперкористувачем, то також буде встановлений ефективний ідентифікатор групи користувача.

### Список параметрів

`group_id`

Ідентифікатор групи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**posix\_setgid()\*\*\*\*

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

-   [posix\_getgrgid()](function.posix-getgrgid.md) \- Повертає інформацію про групу за її ID
-   [posix\_getgid()](function.posix-getgid.md) \- Повертає дійсний ID групи поточного процесу GID
