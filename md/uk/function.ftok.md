Перетворення шляху та ідентифікатора проекту на ключ System V IPC

-   [« Функції семафорів](ref.sem.html)
    
-   [msggetqueue »](function.msg-get-queue.html)
    
-   [PHP Manual](index.html)
    
-   [Функції семафорів](ref.sem.html)
    
-   Перетворення шляху та ідентифікатора проекту на ключ System V IPC
    

# ftok

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ftok — Перетворення шляху та ідентифікатора проекту на ключ System V IPC

### Опис

```methodsynopsis
ftok(string $filename, string $project_id): int
```

Функція перетворює `filename` існуючого, доступного файлу та ідентифікатор проекту в `целое` для використання, наприклад, [shmopopen()](function.shmop-open.html) та інших ключів System V IPC.

### Список параметрів

`filename`

Шлях до файлу

`project_id`

Ідентифікатор проекту Це має бути один символ.

### Значення, що повертаються

У разі успішного виконання повертається створене значення ключа, та `-1` у разі виникнення помилки.

### Дивіться також

-   [shmopopen()](function.shmop-open.html) - Резервування або використання блоку пам'яті, що розділяється
-   [semget()](function.sem-get.html) - Отримання ідентифікатора семафору