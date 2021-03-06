- [« Функції зворотного виклику наскрізного читання кеша](memcached.callbacks.read-through.md)
- [Memcached »](class.memcached.md)

- [PHP Manual](index.md)
- [Memcached](book.memcached.md)
- Підтримка сесій

# Підтримка сесій

Memcached надає власний обробник сесій, який можна
використовувати для зберігання сесійних змінних в memcache. Для цього
використовується повністю окремий екземпляр memcached, тому при
Ви можете використовувати інший пул серверів. Ключі сесії
зберігаються з префіксом `memc.sess.key.`, так що майте це на увазі, якщо
будете використовувати для сесій і звичайного кешування один і той же пул
серверів.

`session.save_handler` string
Встановіть для `memcached` для підтримки обробки сесій.

`session.save_path` string
Задає розділений комами список записів `hostname:port` для
визначення пулу серверів, що обробляють сесії. Наприклад
`sess1:11211, sess2:11211`.
