---
navigation:
  - ref.inotify.md: « Функции Inotify
  - function.inotify-init.html: inotifyinit »
  - index.md: PHP Manual
  - ref.inotify.md: Функции Inotify
title: inotifyaddwatch
---
# inotifyaddwatch

(PECL inotify >= 0.1.2)

inotifyaddwatch — Додати спостерігача для екземпляра inotify

### Опис

```methodsynopsis
inotify_add_watch(resource $inotify_instance, string $pathname, int $mask): int
```

**inotifyaddwatch()** додає нового спостерігача або змінює існуючий для файлу або директорії, заданих у `pathname`

Використання **inotifyaddwatch()** на обстеженні, що вже відстежується, замінить поточного спостерігача. використання константи **`IN_MASK_ADD`** додати (OR) події існуючому спостерігачеві.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotifyinit()](function.inotify-init.md)

`pathname`

Файл або директорія для відстеження

`mask`

Події, які слід відстежувати. Дивіться [Обумовлені константи](inotify.constants.md)

### Значення, що повертаються

Повертає унікальний (в контексті екземпляра inotify) дескриптор спостерігача.

### Дивіться також

-   [inotifyinit()](function.inotify-init.md) - Ініціалізує екземпляр inotify
