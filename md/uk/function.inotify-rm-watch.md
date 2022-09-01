---
navigation:
  - function.inotify-read.html: « inotifyread
  - book.xattr.html: xattr »
  - index.html: PHP Manual
  - ref.inotify.html: Функции Inotify
title: inotifyрмwatch
---
# inotifyрмwatch

(PECL inotify >= 0.1.2)

inotifyрмwatch — Видалити спостерігача

### Опис

```methodsynopsis
inotify_rm_watch(resource $inotify_instance, int $watch_descriptor): bool
```

**inotifyрмwatch()** видаляє спостерігача `watch_descriptor` з екземпляра inotify `inotify_instance`

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotifyinit()](function.inotify-init.html)

`watch_descriptor`

Спостерігач для видалення

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [inotifyinit()](function.inotify-init.html) - Ініціалізує екземпляр inotify
