---
navigation:
  - function.inotify-read.md: « inotify\_read
  - book.xattr.md: xattr »
  - index.md: PHP Manual
  - ref.inotify.md: Функції Inotify
title: inotify\_rm\_watch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inotify\_rm\_watch

(PECL inotify >= 0.1.2)

inotify\_rm\_watch — Видалити спостерігача

### Опис

```methodsynopsis
inotify_rm_watch(resource $inotify_instance, int $watch_descriptor): bool
```

**inotify\_rm\_watch()** видаляє спостерігача `watch_descriptor` з екземпляра inotify `inotify_instance`

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotify\_init()](function.inotify-init.md)

`watch_descriptor`

Спостерігач для видалення

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [inotify\_init()](function.inotify-init.md) \- Ініціалізує екземпляр inotify
