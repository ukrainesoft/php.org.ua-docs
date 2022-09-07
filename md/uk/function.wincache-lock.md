---
navigation:
  - function.wincache-fcache-meminfo.md: « wincachefcachememinfo
  - function.wincache-ocache-fileinfo.md: wincacheocachefileinfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincachelock
---
# wincachelock

(PECL wincache >= 1.1.0)

wincachelock — Отримує ексклюзивне блокування для цього ключа

### Опис

```methodsynopsis
wincache_lock(string $key, bool $isglobal = false): bool
```

Отримує ексклюзивне блокування для цього ключа. Виконання поточного скрипту буде заблоковано, доки блокування не буде отримано. Після отримання блокування інші сценарії, які намагаються запросити блокування за допомогою того ж ключа, будуть заблоковані доти, доки поточний скрипт не зніме блокування за допомогою [wincacheunlock()](function.wincache-unlock.md)

**Увага**

Використання **wincachelock()** і [wincacheunlock()](function.wincache-unlock.md) може викликати взаємне блокування при виконанні скриптів PHP у багатопроцесорному середовищі, такому як FastCGI. Не використовуйте ці функції, якщо ви не впевнені, що це потрібно. Для більшості операцій з кешем користувача ці функції використовувати не обов'язково.

### Список параметрів

`key`

Ім'я ключа в кеші, щоб увімкнути блокування.

`isglobal`

Визначає, чи область блокування загальносистемної чи локальної. Локальні блокування відносяться до пулу додатків у випадку IIS FastCGI або всіх процесів PHP, які мають один і той же ідентифікатор батьківського процесу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **wincachelock()****

```php
<?php
$fp = fopen("/tmp/lock.txt", "r+");
if (wincache_lock(“lock_txt_lock”)) { // получить эксклюзивную блокировку
    ftruncate($fp, 0); // обрезать файл
    fwrite($fp, "Напишите что-нибудь здесь\n");
    wincache_unlock(“lock_txt_lock”); // снять блокировку
} else {
    echo "Не удалось получить блокировку!";
}
fclose($fp);
?>
```

### Дивіться також

-   [wincacheunlock()](function.wincache-unlock.md) - Знімає ексклюзивне блокування цього ключа
-   [wincacheucacheset()](function.wincache-ucache-set.md) - Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincacheucacheget()](function.wincache-ucache-get.md) - Отримує змінну, що зберігається в користувальницькому кеші
-   [wincacheucachedelete()](function.wincache-ucache-delete.md) - Видаляє змінні з користувальницького кешу
-   [wincacheucacheclear()](function.wincache-ucache-clear.md) - Видаляє весь вміст кешу користувача.
-   [wincacheucacheexists()](function.wincache-ucache-exists.md) - Перевіряє, чи існує змінна в кеші користувача
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.md) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.md) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.md) - Отримує інформацію про файли, закешовані в кеші сесії
