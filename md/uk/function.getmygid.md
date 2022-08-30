Отримати GID власника скрипта PHP

-   [« getlastmod](function.getlastmod.html)
    
-   [getmyinode »](function.getmyinode.html)
    
-   [PHP Manual](index.html)
    
-   [Опції PHP/інформаційні функції](ref.info.html)
    
-   Отримати GID власника скрипта PHP
    

# getmygid

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

getmygid — Отримати GID власника скрипта PHP

### Опис

```methodsynopsis
getmygid(): int|false
```

Отримує ідентифікатор групи поточного сценарію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає груповий ідентифікатор поточного скрипту або **`false`** у разі виникнення помилки.

### Дивіться також

-   [getmyuid()](function.getmyuid.html) - Отримання UID власника скрипта PHP
-   [getmypid()](function.getmypid.html) - Отримання ID процесу PHP
-   [getcurrentuser()](function.get-current-user.html) - Отримує ім'я власника поточного скрипту PHP
-   [getmyinode()](function.getmyinode.html) - Отримує значення inode поточного скрипту
-   [getlastmod()](function.getlastmod.html) - Отримує час останньої модифікації сторінки