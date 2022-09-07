---
navigation:
  - function.getmygid.md: « getmygid
  - function.getmypid.md: getmypid »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getmyinode
---
# getmyinode

(PHP 4, PHP 5, PHP 7, PHP 8)

getmyinode — Отримує значення inode поточного скрипту

### Опис

```methodsynopsis
getmyinode(): int|false
```

Отримує inode поточного скрипта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає inode поточного скрипта у вигляді цілого числа або **`false`** у разі помилки.

### Дивіться також

-   [getmygid()](function.getmygid.md) - Отримати GID власника скрипта PHP
-   [getmyuid()](function.getmyuid.md) - Отримання UID власника скрипта PHP
-   [getmypid()](function.getmypid.md) - Отримання ID процесу PHP
-   [getcurrentuser()](function.get-current-user.md) - Отримує ім'я власника поточного скрипту PHP
-   [getlastmod()](function.getlastmod.md) - Отримує час останньої модифікації сторінки
