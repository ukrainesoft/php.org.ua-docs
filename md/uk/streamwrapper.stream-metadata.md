---
navigation:
  - streamwrapper.stream-lock.md: '« streamWrapper::stream\_lock'
  - streamwrapper.stream-open.md: 'streamWrapper::stream\_open »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_metadata'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_metadata

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

streamWrapper::stream\_metadata — Змінює метадані потоку

### Опис

```methodsynopsis
public streamWrapper::stream_metadata(string $path, int $option, mixed $value): bool
```

Цей метод викликається для встановлення метаданих потоку. Він працює, коли над URL потоку виконується одна з таких операцій:

-   [touch()](function.touch.md)
-   [chmod()](function.chmod.md)
-   [chown()](function.chown.md)
-   [chgrp()](function.chgrp.md)

Слід пам'ятати, що деякі з цих операцій можуть бути недоступними у вашій системі.

### Список параметрів

`path`

Шлях до файлу або URL для завдання метаданих. URL має бути відокремлений символами :// Інші формати URL не підтримуються.

`option`

Одне із значень:

-   **`STREAM_META_TOUCH`**(Метод викликається в результаті виклику[touch()](function.touch.md)) .
-   **`STREAM_META_OWNER_NAME`**(Метод викликається в результаті виклику[chown()](function.chown.md)з рядковим аргументом)
-   **`STREAM_META_OWNER`**(Метод викликається в результаті виклику[chown()](function.chown.md)) .
-   **`STREAM_META_GROUP_NAME`**(Метод викликається в результаті виклику[chgrp()](function.chgrp.md)) .
-   **`STREAM_META_GROUP`**(Метод викликається в результаті виклику[chgrp()](function.chgrp.md)) .
-   **`STREAM_META_ACCESS`**(Метод викликається в результаті виклику[chmod()](function.chmod.md)) .

`value`

Якщо `option`принимает значение

-   **`STREAM_META_TOUCH`**: Масив (Array), що складається з двох аргументів функції.[touch()](function.touch.md)
-   **`STREAM_META_OWNER_NAME`** або **`STREAM_META_GROUP_NAME`**: Ім'я власника/групи у вигляді рядка (string).
-   **`STREAM_META_OWNER`** або **`STREAM_META_GROUP`**: Значення власника/групу як цілого числа (int).
-   **`STREAM_META_ACCESS`**: Аргумент функції[chmod()](function.chmod.md) як цілого числа (int).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`**в случае возникновения ошибки. Если`option`не реализован, метод должен вернуть**`false`**

### Дивіться також

-   [touch()](function.touch.md) \- Встановлює час доступу та модифікації файлу
-   [chmod()](function.chmod.md) \- Змінює режим доступу до файлу
-   [chown()](function.chown.md) \- Змінює власника файлу
-   [chgrp()](function.chgrp.md) \- Змінює групу файлу
