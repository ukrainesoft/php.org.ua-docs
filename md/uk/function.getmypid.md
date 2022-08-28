Отримання ID процесу PHP

-   [« getmyinode](function.getmyinode.html)
    
-   [getmyuid »](function.getmyuid.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Отримання ID процесу PHP
    

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

Повертає ідентифікатор процесу PHP або **`false`** у разі виникнення помилки.

### Примітки

**Увага**

Ідентифікатори процесів у системі не є унікальними, тому є слабким джерелом ентропії. Ми не рекомендуємо покладатися на pid у контекстах, що впливають на безпеку.

### Дивіться також

-   [getmygid()](function.getmygid.html) - Отримати GID власника скрипта PHP
-   [getmyuid()](function.getmyuid.html) - Отримання UID власника скрипта PHP
-   [get\_current\_user()](function.get-current-user.html) - Отримує ім'я власника поточного скрипту PHP
-   [getmyinode()](function.getmyinode.html) - Отримує значення inode поточного скрипту
-   [getlastmod()](function.getlastmod.html) - Отримує час останньої модифікації сторінки