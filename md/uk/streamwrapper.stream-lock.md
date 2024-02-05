---
navigation:
  - streamwrapper.stream-flush.md: '« streamWrapper::stream\_flush'
  - streamwrapper.stream-metadata.md: 'streamWrapper::stream\_metadata »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_lock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_lock

(PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_lock — Консультативне блокування файлу

### Опис

```methodsynopsis
public streamWrapper::stream_lock(int $operation): bool
```

Цей метод викликається у відповідь [flock()](function.flock.md), коли викликається [file\_put\_contents()](function.file-put-contents.md) (якщо `flags` містить **`LOCK_EX`** [stream\_set\_blocking()](function.stream-set-blocking.md) або при закритті потоку (**`LOCK_UN`**

### Список параметрів

`operation`

`operation` може приймати одне з наступних значень:

-   \*\*`LOCK_SH`\*\*встановити загальне блокування (для читання).
-   \*\*`LOCK_EX`\*\*встановити ексклюзивне блокування (для запису).
-   \*\*`LOCK_UN`\*\*зняти блокування (загальне або ексклюзивне).
-   **`LOCK_NB`**, якщо ви не хочете, щоб[flock()](function.flock.md)не блокувався під час роботи. (не підтримується у Windows)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викликає помилку \*\*`E_WARNING`\*\*якщо виклик методу не вдався (тобто метод не реалізований).

### Дивіться також

-   [stream\_set\_blocking()](function.stream-set-blocking.md) \- Встановити блокуючий/неблокуючий режим у потоці
-   [flock()](function.flock.md) \- Портоване консультативне блокування файлів
