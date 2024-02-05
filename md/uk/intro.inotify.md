---
navigation:
  - book.inotify.md: « Inotify
  - inotify.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.inotify.md: Inotify
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

Модуль inotify предоставляет функции[inotify\_init()](function.inotify-init.md) [inotify\_add\_watch()](function.inotify-add-watch.md) і [inotify\_rm\_watch()](function.inotify-rm-watch.md)

У той час як функція мови C [inotify\_init()](function.inotify-init.md) повертає дескриптор файлу, функція [inotify\_init()](function.inotify-init.md) PHP повертає потоковий ресурс, який можна використовувати в стандартних функціях, наприклад, [stream\_select()](function.stream-select.md) [stream\_set\_blocking()](function.stream-set-blocking.md) і [fclose()](function.fclose.md)Функция[inotify\_read()](function.inotify-read.md) заміщає спосіб читання подій inotify в C.
