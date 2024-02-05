---
navigation:
  - function.getmypid.md: « getmypid
  - function.getopt.md: getopt »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getmyuid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getmyuid

(PHP 4, PHP 5, PHP 7, PHP 8)

getmyuid - Отримання UID власника скрипта PHP

### Опис

```methodsynopsis
getmyuid(): int|false
```

Отримує ідентифікатор користувача поточного сценарію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор користувача поточного скрипту або \*\*`false`\*\*в случае ошибки.

### Дивіться також

-   [getmygid()](function.getmygid.md) \- Отримати GID власника скрипта PHP
-   [getmypid()](function.getmypid.md) \- Отримання ID процесу PHP
-   [get\_current\_user()](function.get-current-user.md) \- Отримує ім'я власника поточного скрипту PHP
-   [getmyinode()](function.getmyinode.md) \- Отримує значення inode поточного скрипту
-   [getlastmod()](function.getlastmod.md) \- Отримує час останньої модифікації сторінки
