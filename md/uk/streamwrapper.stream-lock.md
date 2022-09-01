---
navigation:
  - streamwrapper.stream-flush.html: '« streamWrapper::streamflush'
  - streamwrapper.stream-metadata.html: 'streamWrapper::streammetadata »'
  - index.html: PHP Manual
  - class.streamwrapper.html: streamWrapper
title: 'streamWrapper::streamlock'
---
# streamWrapper::streamlock

(PHP 5, PHP 7, PHP 8)

streamWrapper::streamlock — Консультативне блокування файлу

### Опис

```methodsynopsis
public streamWrapper::stream_lock(int $operation): bool
```

Цей метод викликається у відповідь [flock()](function.flock.html), коли викликається [fileputcontents()](function.file-put-contents.html) (якщо `flags` містить **`LOCK_EX`** [streamsetblocking()](function.stream-set-blocking.html) або при закритті потоку (**`LOCK_UN`**

### Список параметрів

`operation`

`operation` може приймати одне з наступних значень:

-   **`LOCK_SH`** встановити загальне блокування (для читання).
-   **`LOCK_EX`** встановити ексклюзивне блокування (для запису).
-   **`LOCK_UN`** зняти блокування (загальне або ексклюзивне).
-   **`LOCK_NB`**, якщо ви не хочете, щоб [flock()](function.flock.html) не блокувався під час роботи. (не підтримується у Windows)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку \*\*`E_WARNING`\*\*якщо виклик методу не вдався (тобто метод не реалізований).

### Дивіться також

-   [streamsetblocking()](function.stream-set-blocking.html) - Встановити блокуючий/неблокуючий режим у потоці
-   [flock()](function.flock.html) - Портоване консультативне блокування файлів
