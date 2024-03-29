---
navigation:
  - function.getlastmod.md: « getlastmod
  - function.getmyinode.md: getmyinode »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getmygid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getmygid

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

getmygid — Отримати GID власника скрипта PHP

### Опис

```methodsynopsis
getmygid(): int|false
```

Отримує ідентифікатор групи поточного сценарію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає груповий ідентифікатор поточного скрипту або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [getmyuid()](function.getmyuid.md) \- Отримання UID власника скрипта PHP
-   [getmypid()](function.getmypid.md) \- Отримання ID процесу PHP
-   [get\_current\_user()](function.get-current-user.md) \- Отримує ім'я власника поточного скрипту PHP
-   [getmyinode()](function.getmyinode.md) \- Отримує значення inode поточного скрипту
-   [getlastmod()](function.getlastmod.md) \- Отримує час останньої модифікації сторінки
