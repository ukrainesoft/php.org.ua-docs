Знімає ексклюзивне блокування цього ключа

-   [« wincache\_ucache\_set](function.wincache-ucache-set.html)
    
-   [Сборка для Windows »](wincache.win32build.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Знімає ексклюзивне блокування цього ключа
    

# wincacheunlock

(PECL wincache >= 1.1.0)

wincacheunlock — Знімає ексклюзивне блокування цього ключа

### Опис

```methodsynopsis
wincache_unlock(string $key): bool
```

Знімає виняткове блокування, яке було отримано для даного ключа за допомогою [wincache\_lock()](function.wincache-lock.html). Якщо будь-який інший процес був заблокований в очікуванні блокування цього ключа, цей процес зможе отримати блокування.

**Увага**

Використання [wincache\_lock()](function.wincache-lock.html) і **wincacheunlock()** може викликати взаємне блокування при виконанні скриптів PHP у багатопроцесорному середовищі, такому як FastCGI. Не використовуйте ці функції, якщо ви не впевнені, що це потрібно. Для більшості операцій з кешем користувача ці функції використовувати не обов'язково.

### Список параметрів

`key`

Ім'я ключа у кеші для зняття блокування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **wincacheunlock()****

```php
<?php
$fp = fopen("/tmp/lock.txt", "r+");
if (wincache_lock(“lock_txt_lock”)) { // получить эксклюзивную блокировку
    ftruncate($fp, 0); // обрезать файл
    fwrite($fp, "Напишите что-нибудь здесь\n");
    wincache_unlock(“lock_txt_lock”); // снять блокировку
} else {
    echo "Не удалось получить блокировку!";
}
fclose($fp);
?>
```

### Дивіться також

-   [wincache\_lock()](function.wincache-lock.html) - Отримує ексклюзивне блокування для цього ключа
-   [wincache\_ucache\_set()](function.wincache-ucache-set.html) - Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincache\_ucache\_get()](function.wincache-ucache-get.html) - Отримує змінну, що зберігається в користувальницькому кеші
-   [wincache\_ucache\_delete()](function.wincache-ucache-delete.html) - Видаляє змінні з користувальницького кешу
-   [wincache\_ucache\_clear()](function.wincache-ucache-clear.html) - Видаляє весь вміст кешу користувача.
-   [wincache\_ucache\_exists()](function.wincache-ucache-exists.html) - Перевіряє, чи існує змінна в кеші користувача
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.html) - Отримує інформацію про файли, закешовані в кеші сесії