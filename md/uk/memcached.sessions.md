---
navigation:
  - memcached.callbacks.read-through.md: Функції зворотного виклику наскрізного читання кешу
  - class.memcached.md: Memcached »
  - index.md: PHP Manual
  - book.memcached.md: Memcached
title: Підтримка сесій
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Підтримка сесій

Memcached надає власний обробник сесій, який можна використовувати для зберігання сесійних змінних у memcache. Для цього використовується повністю окремий екземпляр memcached, тому за потреби ви можете використовувати інший пул серверів. Ключі сесії зберігаються із префіксом `memc.sess.key.`, так що майте на увазі, якщо будете використовувати для сесій і звичайного кешування один і той же пул серверів.

`session.save_handler`string

Установите для`memcached`для поддержки обработки сессий.

`session.save_path`string

Задає розділений комами список записів `hostname:port` для визначення пулу серверів, що обробляють сесії. Наприклад `"sess1:11211, sess2:11211"`
