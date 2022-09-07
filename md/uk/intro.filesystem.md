---
navigation:
  - book.filesystem.md: « Файлова система
  - filesystem.setup.md: Встановлення та налаштування »
  - index.md: PHP Manual
  - book.filesystem.md: Файлова система
title: Вступ
---
# Вступ

Цей модуль не потребує встановлення ніяких зовнішніх бібліотек, але якщо вам потрібна підтримка LFS (великих файлів) в Linux, то вам буде потрібна сучасна версія glibc і вам слід збирати PHP з включенням наступних прапорів у CFLAGS: `-D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64`
