---
navigation:
  - function.wincache-ucache-set.md: « wincacheucacheset
  - wincache.win32build.md: Сборка для Windows »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacheunlock
---
# wincacheunlock

(PECL wincache >= 1.1.0)

wincacheunlock — Знімає ексклюзивне блокування цього ключа

### Опис

```methodsynopsis
wincache_unlock(string $key): bool
```

Знімає виняткове блокування, яке було отримано для даного ключа за допомогою [wincachelock()](function.wincache-lock.md). Якщо будь-який інший процес був заблокований в очікуванні блокування цього ключа, цей процес зможе отримати блокування.

**Увага**

Використання [wincachelock()](function.wincache-lock.md) і **wincacheunlock()** може викликати взаємне блокування при виконанні скриптів PHP у багатопроцесорному середовищі, такому як FastCGI. Не використовуйте ці функції, якщо ви не впевнені, що це потрібно. Для більшості операцій з кешем користувача ці функції використовувати не обов'язково.

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

-   [wincachelock()](function.wincache-lock.md) - Отримує ексклюзивне блокування для цього ключа
-   [wincacheucacheset()](function.wincache-ucache-set.md) - Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincacheucacheget()](function.wincache-ucache-get.md) - Отримує змінну, що зберігається в користувальницькому кеші
-   [wincacheucachedelete()](function.wincache-ucache-delete.md) - Видаляє змінні з користувальницького кешу
-   [wincacheucacheclear()](function.wincache-ucache-clear.md) - Видаляє весь вміст кешу користувача.
-   [wincacheucacheexists()](function.wincache-ucache-exists.md) - Перевіряє, чи існує змінна в кеші користувача
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.md) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.md) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.md) - Отримує інформацію про файли, закешовані в кеші сесії
