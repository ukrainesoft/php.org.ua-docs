---
navigation:
  - function.inotify-queue-len.md: « inotify\_queue\_len
  - function.inotify-rm-watch.md: inotify\_rm\_watch »
  - index.md: PHP Manual
  - ref.inotify.md: Функції Inotify
title: inotify\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inotify\_read

(PECL inotify >= 0.1.2)

inotify\_read — Читає повідомлення, що очікують, з черги

### Опис

```methodsynopsis
inotify_read(resource $inotify_instance): array
```

Читає повідомлення з черги.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotify\_init()](function.inotify-init.md)

### Значення, що повертаються

Масив подій inotify або **`false`**, якщо подій у черзі немає та `inotify_instance` не блокуючий. Кожен елемент масиву складається з:

-   wd - дескриптор спостерігача, повернутий[inotify\_add\_watch()](function.inotify-add-watch.md)
-   mask - бітова маска[подій](inotify.constants.md)
-   cookie – унікальний ідентифікатор для об'єднання пов'язаних подій (наприклад\*\*`IN_MOVE_FROM`** і **`IN_MOVE_TO`\*\*) .
-   name - ім'я файлу (наприклад якщо в директорії, що спостерігається, змінився файл)

### Дивіться також

-   [inotify\_init()](function.inotify-init.md) \- Ініціалізує екземпляр inotify
-   [stream\_select()](function.stream-select.md) \- Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [stream\_set\_blocking()](function.stream-set-blocking.md) \- Встановити блокуючий/неблокуючий режим у потоці
-   [inotify\_queue\_len()](function.inotify-queue-len.md) \- Повертає кількість очікуваних подій у черзі
