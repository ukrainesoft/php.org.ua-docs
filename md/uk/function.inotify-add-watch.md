---
navigation:
  - ref.inotify.md: « Функції Inotify
  - function.inotify-init.md: inotify\_init »
  - index.md: PHP Manual
  - ref.inotify.md: Функції Inotify
title: inotify\_add\_watch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inotify\_add\_watch

(PECL inotify >= 0.1.2)

inotify\_add\_watch — Додати спостерігача для екземпляра inotify

### Опис

```methodsynopsis
inotify_add_watch(resource $inotify_instance, string $pathname, int $mask): int
```

**inotify\_add\_watch()** додає нового спостерігача або змінює існуючий для файлу або директорії, заданих у `pathname`

Использование**inotify\_add\_watch()** на обстеженні, що вже відстежується, замінить поточного спостерігача. використання константи **`IN_MASK_ADD`** додати (OR) події існуючому спостерігачеві.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotify\_init()](function.inotify-init.md)

`pathname`

Файл або директорія для відстеження

`mask`

Події, які слід відстежувати. Дивіться [Обумовлені константи](inotify.constants.md)

### Значення, що повертаються

Повертає унікальний (в контексті екземпляра inotify) дескриптор спостерігача.

### Дивіться також

-   [inotify\_init()](function.inotify-init.md) \- Ініціалізує екземпляр inotify
