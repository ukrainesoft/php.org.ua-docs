---
navigation:
  - function.openal-source-stop.md: « openalsourcestop
  - refs.remote.auth.md: Служби аутентифікації »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalstream
---
# openalstream

(PECL openal >= 0.1.0)

openalstream — Почати потокову передачу з джерела

### Опис

```methodsynopsis
openal_stream(resource $source, int $format, int $rate): resource|false
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.md)

`format`

Формат даних `data`, представлений однією з констант: **`AL_FORMAT_MONO8`** **`AL_FORMAT_MONO16`** **`AL_FORMAT_STEREO8`** і **`AL_FORMAT_STEREO16`**

`rate`

Частота передачі в потік задається в герцах.

### Значення, що повертаються

Повертає ресурс потоку у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcecreate()](function.openal-source-create.md) - Згенерувати джерело ресурсу
-   [fwrite()](function.fwrite.md) - Бінарно-безпечний запис у файл
