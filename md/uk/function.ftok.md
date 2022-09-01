---
navigation:
  - ref.sem.html: « Функції семафорів
  - function.msg-get-queue.html: msggetqueue »
  - index.html: PHP Manual
  - ref.sem.html: Функції семафорів
title: ftok
---
# ftok

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ftok — Перетворення шляху та ідентифікатора проекту на ключ System V IPC

### Опис

```methodsynopsis
ftok(string $filename, string $project_id): int
```

Функція перетворює `filename` існуючого, доступного файлу та ідентифікатор проекту в `целое` для використання, наприклад, [shmopopen()](function.shmop-open.md) та інших ключів System V IPC.

### Список параметрів

`filename`

Шлях до файлу

`project_id`

Ідентифікатор проекту Це має бути один символ.

### Значення, що повертаються

У разі успішного виконання повертається створене значення ключа, та `-1` у разі виникнення помилки.

### Дивіться також

-   [shmopopen()](function.shmop-open.md) - Резервування або використання блоку пам'яті, що розділяється
-   [semget()](function.sem-get.md) - Отримання ідентифікатора семафору
