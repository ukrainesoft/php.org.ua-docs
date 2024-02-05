---
navigation:
  - function.wincache-fcache-meminfo.md: « wincache\_fcache\_meminfo
  - function.wincache-ocache-fileinfo.md: wincache\_ocache\_fileinfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_lock
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_lock

(PECL wincache >= 1.1.0)

wincache\_lock — Отримує ексклюзивне блокування для цього ключа

### Опис

```methodsynopsis
wincache_lock(string $key, bool $isglobal = false): bool
```

Отримує ексклюзивне блокування для цього ключа. Виконання поточного скрипту буде заблоковано, доки блокування не буде отримано. Після отримання блокування інші сценарії, які намагаються запросити блокування за допомогою того ж ключа, будуть заблоковані доти, доки поточний скрипт не зніме блокування за допомогою [wincache\_unlock()](function.wincache-unlock.md)

**Увага**

Использование\*\*wincache\_lock()\*\*и[wincache\_unlock()](function.wincache-unlock.md) може викликати взаємне блокування під час виконання скриптів PHP у багатопроцесорному середовищі, такому як FastCGI. Не використовуйте ці функції, якщо ви не впевнені, що це потрібно. Для більшості операцій з кешем користувача ці функції використовувати не обов'язково.

### Список параметрів

`key`

Ім'я ключа в кеші, щоб увімкнути блокування.

`isglobal`

Визначає, чи область блокування загальносистемної чи локальної. Локальні блокування відносяться до пулу додатків у випадку IIS FastCGI або до всіх процесів PHP, які мають той самий ідентифікатор батьківського процесу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**wincache\_lock()\*\*\*\*

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

-   [wincache\_unlock()](function.wincache-unlock.md) \- Знімає ексклюзивне блокування цього ключа
-   [wincache\_ucache\_set()](function.wincache-ucache-set.md) \- Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincache\_ucache\_get()](function.wincache-ucache-get.md) \- Отримує змінну, що зберігається в користувальницькому кеші
-   [wincache\_ucache\_delete()](function.wincache-ucache-delete.md) \- Видаляє змінні з користувальницького кешу
-   [wincache\_ucache\_clear()](function.wincache-ucache-clear.md) \- Видаляє весь вміст користувальницького кешу
-   [wincache\_ucache\_exists()](function.wincache-ucache-exists.md) \- Перевіряє, чи існує змінна в кеші користувача
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
