---
navigation:
  - ref.sem.md: « Функції семафорів
  - function.msg-get-queue.md: msg\_get\_queue »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: ftok
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftok

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ftok — Перетворює шлях та ідентифікатор проекту на ключ System V IPC

### Опис

```methodsynopsis
ftok(string $filename, string $project_id): int
```

Функція перетворює шлях `filename` існуючого доступного файлу та ідентифікатор проекту в `ціле число` для дзвінка, наприклад, у функції [shmop\_open()](function.shmop-open.md) та інших ключів System V IPC.

### Список параметрів

`filename`

Шлях до файлу

`project_id`

Ідентифікатор проекту Це має бути один символ.

### Значення, що повертаються

У разі успішного виконання повертає створене значення ключа, та `-1`в случае возникновения ошибки.

### Дивіться також

-   [shmop\_open()](function.shmop-open.md) \- Резервування або використання блоку пам'яті, що розділяється
-   [sem\_get()](function.sem-get.md) \- Отримання ідентифікатора семафору
