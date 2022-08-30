Отримує час останньої модифікації сторінки

-   [« getenv](function.getenv.html)
    
-   [getmygid »](function.getmygid.html)
    
-   [PHP Manual](index.html)
    
-   [Опції PHP/інформаційні функції](ref.info.html)
    
-   Отримує час останньої модифікації сторінки
    

# getlastmod

(PHP 4, PHP 5, PHP 7, PHP 8)

getlastmod — Отримує час останньої модифікації сторінки

### Опис

```methodsynopsis
getlastmod(): int|false
```

Отримує час останньої модифікації запущеного сценарію.

Якщо потрібно отримати час для модифікації довільного файлу, використовуйте функцію [filemtime()](function.filemtime.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час останньої модифікації поточної сторінки. Значення є міткою часу Unix, що підходить для функції [date()](function.date.html). Функція поверне **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **getlastmod()****

```php
<?php
// Выводит нечто вроде 'Последнее изменение: March 04 1998 20:43:59.'
echo "Последнее изменение: " . date ("F d Y H:i:s.", getlastmod());
?>
```

### Дивіться також

-   [date()](function.date.html) - Форматує тимчасову мітку Unix
-   [getmyuid()](function.getmyuid.html) - Отримання UID власника скрипта PHP
-   [getmygid()](function.getmygid.html) - Отримати GID власника скрипта PHP
-   [getcurrentuser()](function.get-current-user.html) - Отримує ім'я власника поточного скрипту PHP
-   [getmyinode()](function.getmyinode.html) - Отримує значення inode поточного скрипту
-   [getmypid()](function.getmypid.html) - Отримання ID процесу PHP
-   [filemtime()](function.filemtime.html) - Повертає час останньої зміни файлу