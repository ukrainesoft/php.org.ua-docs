---
navigation:
  - function.getmyinode.md: « getmyinode
  - function.getmyuid.md: getmyuid »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getmypid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getmypid

(PHP 4, PHP 5, PHP 7, PHP 8)

getmypid - Отримання ID процесу PHP

### Опис

```methodsynopsis
getmypid(): int|false
```

Отримує ідентифікатор PHP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор процесу PHP або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

**Увага**

Ідентифікатори процесів у системі не є унікальними, тому є слабким джерелом ентропії. Ми не рекомендуємо покладатися на pid у контекстах, що впливають на безпеку.

### Дивіться також

-   [getmygid()](function.getmygid.md) \- Отримати GID власника скрипта PHP
-   [getmyuid()](function.getmyuid.md) \- Отримання UID власника скрипта PHP
-   [get\_current\_user()](function.get-current-user.md) \- Отримує ім'я власника поточного скрипту PHP
-   [getmyinode()](function.getmyinode.md) \- Отримує значення inode поточного скрипту
-   [getlastmod()](function.getlastmod.md) \- Отримує час останньої модифікації сторінки
