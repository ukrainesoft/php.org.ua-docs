---
navigation:
  - book.inotify.md: « Inotify
  - inotify.setup.md: Встановлення та налаштування »
  - index.md: PHP Manual
  - book.inotify.md: Inotify
title: Вступ
---
# Вступ

Модуль inotify надає функції [inotifyinit()](function.inotify-init.md) [inotifyaddwatch()](function.inotify-add-watch.md) і [inotifyрмwatch()](function.inotify-rm-watch.md)

У той час як функція мови C [inotifyinit()](function.inotify-init.md) повертає дескриптор файлу, функція [inotifyinit()](function.inotify-init.md) PHP повертає потоковий ресурс, який можна використовувати в стандартних функціях, наприклад, [streamselect()](function.stream-select.md) [streamsetblocking()](function.stream-set-blocking.md) і [fclose()](function.fclose.md). Функція [inotifyread()](function.inotify-read.md) замінює спосіб читання подій inotify в C.
