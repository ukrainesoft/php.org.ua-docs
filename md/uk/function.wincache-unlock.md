---
navigation:
  - function.wincache-ucache-set.md: « wincache\_ucache\_set
  - wincache.win32build.md: Складання для Windows »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_unlock
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_unlock

(PECL wincache >= 1.1.0)

wincache\_unlock — Знімає ексклюзивне блокування цього ключа

### Опис

```methodsynopsis
wincache_unlock(string $key): bool
```

Знімає виняткове блокування, яке було отримано для даного ключа за допомогою [wincache\_lock()](function.wincache-lock.md). Якщо будь-який інший процес був заблокований в очікуванні блокування цього ключа, цей процес зможе отримати блокування.

**Увага**

Использование[wincache\_lock()](function.wincache-lock.md)и**wincache\_unlock()** може викликати взаємне блокування під час виконання скриптів PHP у багатопроцесорному середовищі, такому як FastCGI. Не використовуйте ці функції, якщо ви не впевнені, що це потрібно. Для більшості операцій з кешем користувача ці функції використовувати не обов'язково.

### Список параметрів

`key`

Ім'я ключа у кеші для зняття блокування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**wincache\_unlock()\*\*\*\*

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

-   [wincache\_lock()](function.wincache-lock.md) \- Отримує ексклюзивне блокування для цього ключа
-   [wincache\_ucache\_set()](function.wincache-ucache-set.md) \- Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincache\_ucache\_get()](function.wincache-ucache-get.md) \- Отримує змінну, що зберігається в користувальницькому кеші
-   [wincache\_ucache\_delete()](function.wincache-ucache-delete.md) \- Видаляє змінні з користувальницького кешу
-   [wincache\_ucache\_clear()](function.wincache-ucache-clear.md) \- Видаляє весь вміст користувальницького кешу
-   [wincache\_ucache\_exists()](function.wincache-ucache-exists.md) \- Перевіряє, чи існує змінна в кеші користувача
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
