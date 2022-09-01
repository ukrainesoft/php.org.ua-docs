---
navigation:
  - streamwrapper.stream-lock.html: '« streamWrapper::streamlock'
  - streamwrapper.stream-open.html: 'streamWrapper::streamopen »'
  - index.html: PHP Manual
  - class.streamwrapper.html: streamWrapper
title: 'streamWrapper::streammetadata'
---
# streamWrapper::streammetadata

(PHP 5> = 5.4.0, PHP 7, PHP 8)

streamWrapper::streammetadata — Змінює метадані потоку

### Опис

```methodsynopsis
public streamWrapper::stream_metadata(string $path, int $option, mixed $value): bool
```

Цей метод викликається для встановлення метаданих потоку. Він працює, коли над URL потоку виконується одна з таких операцій:

-   [touch()](function.touch.html)
-   [chmod()](function.chmod.html)
-   [chown()](function.chown.html)
-   [chgrp()](function.chgrp.html)

Слід пам'ятати, що деякі з цих операцій можуть бути недоступними у вашій системі.

### Список параметрів

`path`

Шлях до файлу або URL для завдання метаданих. URL має бути відокремлений символами :// Інші формати URL не підтримуються.

`option`

Одне із значень:

-   **`STREAM_META_TOUCH`** (Метод викликається в результаті виклику [touch()](function.touch.html)
-   **`STREAM_META_OWNER_NAME`** (Метод викликається в результаті виклику [chown()](function.chown.html) з рядковим аргументом)
-   **`STREAM_META_OWNER`** (Метод викликається в результаті виклику [chown()](function.chown.html)
-   **`STREAM_META_GROUP_NAME`** (Метод викликається в результаті виклику [chgrp()](function.chgrp.html)
-   **`STREAM_META_GROUP`** (Метод викликається в результаті виклику [chgrp()](function.chgrp.html)
-   **`STREAM_META_ACCESS`** (Метод викликається в результаті виклику [chmod()](function.chmod.html)

`value`

Якщо `option` приймає значення

-   **`STREAM_META_TOUCH`**: Масив (Array), що складається з двох аргументів функції. [touch()](function.touch.html)
-   **`STREAM_META_OWNER_NAME`** або **`STREAM_META_GROUP_NAME`**: Ім'я власника/групи у вигляді рядка (string).
-   **`STREAM_META_OWNER`** або **`STREAM_META_GROUP`**: Значення власника/групу як цілого числа (int).
-   **`STREAM_META_ACCESS`**: Аргумент функції [chmod()](function.chmod.html) як цілого числа (int).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо `option` не реалізований, метод має повернути **`false`**

### Дивіться також

-   [touch()](function.touch.html) - Встановлює час доступу та модифікації файлу
-   [chmod()](function.chmod.html) - Змінює режим доступу до файлу
-   [chown()](function.chown.html) - Змінює власника файлу
-   [chgrp()](function.chgrp.html) - Змінює групу файлу
